# EEG - Mini Project: Classification of EEG Oddball Signals  
### **Group 10 — Members**
- **Pham Quan** (23020418)  
- **Pham Hai Tien** (23020425)  
- **Chu Thanh Tung** (23020431)  
- **Nguyen Tran Huy** (23020378)  
- **Dam Le Minh Quan** (23020416)  
- **Ngo Nguyen Khai Hung** (23020382)  

---

This project investigates single-trial P300 detection using both traditional machine-learning pipelines and deep learning models, applied on a 42-subject auditory oddball EEG dataset.  
We build a unified framework combining spatial filtering (xDAWN), temporal modeling (HMM), ERP features, and end-to-end CNNs to compare accuracy, robustness, and computational efficiency.

---

##  Pipeline

### **Preprocessing**
- 1–30 Hz bandpass filtering  
- Artifact rejection  
- Baseline correction  
- CAR referencing  

### **Feature Extraction**
- **xDAWN** → 6 spatial components (774 temporal features)  
- **ERP amplitude** (250–500 ms)  
- **HMM** → temporal likelihood features  
- **Final feature vector**: **777 dimensions**

### **Classical ML Models**
- LDA  
- Logistic Regression  
- SVM  
- Random Forest  
- Gradient Boosting  
- XGBoost  

### **Deep Learning Models**
- EEGNet  
- ShallowConvNet  
- DeepConvNet (trained on raw EEG)

---

##  Experiments
- **Within-subject ML**: subject-specific xDAWN + ML  
- **Cross-subject DL**: train on 36 subjects, test on 6 unseen subjects  

---

##  Key Results
- **Traditional ML**: ~77.5% accuracy, fast training (~10s/subject)  
- **Deep Learning**: up to **94.6% accuracy** (EEGNet & DeepConvNet), slower (~150s/subject)  
- **HMM** improves ML models by ~0.5–1.5%  
- DL models reduce inter-subject variability and generalize better  

---

##  Insights
- CNNs leverage full spatiotemporal information → higher accuracy  
- ML methods are interpretable & fast → suitable for quick calibration or clinical BCIs  
- DL is ideal for offline analysis or scenarios with sufficient data  

---

##  Acknowledgment
We would like to express our sincere gratitude to our **professors and instructors** for their dedicated teaching, guidance, and continuous support throughout the development of this project.  
Their expertise and encouragement have been invaluable and greatly contributed to the successful completion of our work.  
