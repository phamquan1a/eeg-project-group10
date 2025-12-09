# EEG - Mini Project: Classification of EEG Oddball Signals  

This project is the result of our group's work for the Computational Neuroscience and Applications course. We would like to express our sincere gratitude to Professor Guy Nagels and Professor Nguyen Linh Trung for their dedicated guidance and support throughout this project.
This project investigates single-trial P300 detection using both traditional machine-learning pipelines and deep learning models, applied on a 42-subject auditory oddball EEG dataset.  
We build a unified framework combining spatial filtering (xDAWN), temporal modeling (HMM), ERP features, and end-to-end CNNs to compare accuracy, robustness, and computational efficiency.

### **Group 10 - Members**
- **Pham Quan** (23020418)  
- **Pham Hai Tien** (23020425)  
- **Chu Thanh Tung** (23020431)  
- **Nguyen Tran Huy** (23020378)  
- **Dam Le Minh Quan** (23020416)  
- **Ngo Nguyen Khai Hung** (23020382)  

##  Pipeline

### **Preprocessing**
- bandpass filtering  
- Artifact rejection  
- Baseline correction  
- CAR referencing  

### **Feature Extraction**
- xDAWN
- ERP amplitude
- HMM
  
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
- DeepConvNet

---

##  Experiments
- **Within-subject ML**: subject-specific xDAWN + ML  
- **Cross-subject ML & DL**: train on 36 subjects, test on 6 unseen subjects  

---

##  Results
Traditional machine learning methods typically achieve around 77.5% accuracy, while deep learning approaches—particularly models like EEGNet and DeepConvNet—can reach performance levels of up to 94.6%. Incorporating HMM-based features further boosts ML performance by approximately 0.5–1.5%. Moreover, deep learning models tend to reduce inter-subject variability and offer better generalization across different participants.

---

##  Insights
CNNs can exploit the full spatiotemporal structure of EEG signals, often achieving higher accuracy as a result. In contrast, traditional machine learning methods are fast and interpretable, making them well-suited for rapid calibration or clinical BCI applications. Deep learning models, meanwhile, are ideal for offline analysis or scenarios where sufficient data are available to fully leverage their representational power.


