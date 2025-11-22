# ML_Bearing-Failure
This project is my attempt to build a simple, fast machine-learning pipeline that can detect early bearing faults using 3-axis vibration data. I’m exploring how AI can support real mechanical systems, especially rotating machinery where failure is expensive but highly predictable from vibration patterns.
Right now, the project focuses on preprocessing and feature extraction — turning raw accelerometer readings into meaningful signals that a model can learn from.
By extracting statistical features such as RMS, kurtosis, skewness, and crest factor from segmented vibration signals, the model can distinguish between normal and faulty bearing conditions, aiding in early fault detection and predictive maintenance.
✔ Data ingestion
Normal + faulty datasets loaded from raw CSV files (full-load rotating shaft setup).
✔ Automatic time-windowing
The raw vibration stream is segmented into fixed-length windows that represent “1 second” snapshots of machine behavior.
✔ Feature extraction pipeline
For each window, I generate vibration features commonly used in condition monitoring:
Mean
Standard deviation
RMS
Skewness
Kurtosis
Crest factor
These features form the core dataset I'm currently working with.
✔ Labeled, ML-ready dataset
Both the normal and faulty signals are processed into a clean feature table that a model can train on immediately.

What I’m Building Next
This repo is still active — I’m currently adding:
Baseline models (Random Forest, XGBoost, SVM)
A small deep model for comparison
Evaluation pipeline + confusion matrix
Optional Streamlit demo for real-time prediction
This is going to double as a project I submit to SPE NAICE, so I’m pushing toward getting measurable results soon.

Why This Project
I’m exploring the intersection of AI and mechanical engineering — especially how ML can support diagnostics, reliability, and smarter machine operation.
This project is my hands-on way of:
Working directly with real sensor data
Building a pipeline end-to-end
Applying AI to a real mechanical problem
Practicing fast iteration and experimentation as a builder

Data source: Patel, Jaheer  (2022), “3 Axis Vibration Dataset of  Bearing of Induction Motor under Different Loading Conditions ”, Mendeley Data, V1, doi: 10.17632/ckjz2r3nvc.1
