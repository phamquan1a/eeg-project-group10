# EEG - Mini Project: Classification of EEG Oddball Signals  

This project is the result of our group's work for the Computational Neuroscience and Applications course. We would like to express our sincere gratitude to Professor Guy Nagels and Professor Nguyen Linh Trung for their dedicated guidance and support throughout this project.

### **Group 10 - Members**
- **Pham Quan** (23020418)  
- **Pham Hai Tien** (23020425)  
- **Chu Thanh Tung** (23020431)  
- **Nguyen Tran Huy** (23020378)  
- **Dam Le Minh Quan** (23020416)  
- **Ngo Nguyen Khai Hung** (23020382)  

##  Pipeline

### **Preprocessing**
The EEG signals are preprocessed using standard steps, including bandpass filtering, artifact rejection, baseline correction, and common average referencing. 

### **Feature Extraction**
Feature extraction combines spatial, temporal, and probabilistic representations. xDAWN is applied to enhance event-related responses, ERP amplitudes are measured within the relevant time window, and an HMM is used to generate temporal likelihood–based features. The HMM component is included to evaluate whether its timeseries representations provide additional value beyond the standard ERP-based features.
  
### **Classical ML Models**
A range of classical machine-learning models is used to classify frequent versus target trials under a balanced design. The models include LDA, Logistic Regression, SVM, Random Forest, Gradient Boosting, and XGBoost.
 

### **Deep Learning Models**
For comparison with traditional approaches, several deep-learning architectures tailored for EEG data are also implemented. These include EEGNet, ShallowConvNet, and DeepConvNet.


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


