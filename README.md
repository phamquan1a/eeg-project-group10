# Project Overview: P300 Detection with xDAWN, HMM & Deep Learning

This project investigates single-trial P300 detection using both traditional machine-learning pipelines and deep learning models, applied on a 42-subject auditory oddball EEG dataset.
We build a unified framework combining spatial filtering (xDAWN), temporal modeling (HMM), ERP features, and end-to-end CNNs to compare accuracy, robustness, and computational efficiency.

# Pipeline

Preprocessing: 1–30 Hz filtering, artifact rejection, baseline correction, CAR referencing.

Feature extraction:

xDAWN → 6 spatial components (774 temporal features)

P300 ERP amplitude (250–500 ms)

HMM → temporal likelihood features
→ Final feature vector: 777 dimensions

Classical ML models: LDA, LogReg, SVM, RandomForest, GradientBoosting, XGBoost.

Deep Learning models: EEGNet, ShallowConvNet, DeepConvNet trained on raw EEG.

# Experiments

Within-subject ML evaluation: subject-specific xDAWN + ML.

Cross-subject DL evaluation: train on 36 subjects, test on 6 unseen subjects.

# Key Results

Traditional ML: ~77.5% accuracy, fast training (~10s/subject).

Deep Learning: up to 94.6% accuracy (EEGNet & DeepConvNet), but slower (~150s/subject).

HMM augmentation improves ML models by ~0.5–1.5%.

Deep learning strongly reduces inter-subject variability and generalizes better.

# Insights

CNNs leverage full spatiotemporal information → much higher accuracy.

ML methods are interpretable and fast → suitable for quick calibration or clinical BCIs.

Deep models are ideal for offline analysis or scenarios with sufficient data.
