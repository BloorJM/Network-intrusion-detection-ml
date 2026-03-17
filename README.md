# Network Intrusion Detection using Machine Learning
**MSc Computer Science with Cyber Security — University of York (2025)**

## Overview
This project builds and compares three machine learning models for detecting 
network intrusions and classifying attack traffic, using the CICIDS 2017 dataset 
— a widely used benchmark in cybersecurity research containing real-world network 
traffic with labelled attack categories.

The goal was to evaluate which model architecture is most suitable for 
anomaly-based intrusion detection in a real-world SOC context.

## Models Compared
| Model | Architecture | Best Validation Accuracy |
|---|---|---|
| CNN | 1D Convolutional Neural Network | **99.5%** |
| RNN | Recurrent Neural Network | ~97.8% |
| Random Forest | Ensemble Decision Trees | — |

## Attack Types Detected
The models were trained to classify the following traffic categories from CICIDS 2017:
- Benign (normal traffic)
- DDoS
- PortScan
- Brute Force
- Web Attacks
- Botnet
- Infiltration

## Tech Stack
- Python, Jupyter Notebook
- TensorFlow / Keras (CNN, RNN)
- Scikit-learn (Random Forest, feature selection, preprocessing)
- Pandas, NumPy, Matplotlib, Seaborn

## Dataset
[CICIDS 2017](https://www.unb.ca/cic/datasets/ids-2017.html) — Canadian Institute 
for Cybersecurity Intrusion Detection dataset. Not included in this repo due to 
size; download directly from the link above.

## Key Findings
- The CNN model outperformed both the RNN and Random Forest across all metrics
- Feature selection using both univariate methods and tree-based importance 
  ranking was used to reduce dimensionality before training
- Results suggest CNN architectures are well-suited to network flow classification 
  tasks relevant to automated alert triage in SOC environments
