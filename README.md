# NetGuard-QoS-IDS

## Project Title

NetGuard: QoS-Aware Network Intrusion Detection Using Comparative Machine Learning

## Overview

NetGuard-QoS-IDS is a B.Tech CSE (23CSE301 Machine Learning Capstone) project that performs comparative machine-learning analysis across three independent tracks:
- **Regression** — Predicting continuous network QoS and traffic degradation metrics.
- **Classification** — Classifying network attacks and intrusion activities into discrete attack categories.
- **Clustering** — Unsupervised grouping and structural analysis of network traffic behaviour.

Each machine learning track is conducted independently using a separate, dedicated dataset:
- **Regression Track**: UNSW-NB15 dataset
- **Classification Track**: CIC-IDS2017 dataset
- **Clustering Track**: CTU-13 dataset

## Problem Statement

Modern network infrastructures require automated, machine-learning-driven monitoring to maintain Quality of Service (QoS) and defend against malicious cyber threats. This capstone project addresses three core operational challenges in network traffic analysis:
- **QoS & Traffic Degradation Prediction**: Estimating continuous performance indicators (such as packet loss or latency metrics) from flow characteristics to proactively optimize network resources.
- **Network Intrusion Classification**: Accurately distinguishing benign traffic from diverse attack vectors (e.g., DoS, Port Scans, Brute Force, Malware) across multi-class scenarios.
- **Unsupervised Traffic Behaviour Profiling**: Discovering hidden traffic structures, anomaly patterns, and operational clusters without prior label annotations.

## Datasets

| Track | Dataset | Purpose |
|---|---|---|
| Regression | UNSW-NB15 | Network QoS/packet-loss prediction |
| Classification | CIC-IDS2017 | Network attack classification |
| Clustering | CTU-13 | Unsupervised network traffic behaviour analysis |

*Note: Raw dataset files are intentionally excluded from the Git repository due to dataset size and distribution guidelines. Instructions for downloading and placing datasets locally are provided below.*

## Project Structure

```text
NetGuard-QoS-IDS/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   ├── regression/
│   │   └── README.md
│   │
│   ├── classification/
│   │   └── README.md
│   │
│   └── clustering/
│       └── README.md
│
├── notebooks/
│   ├── regression.ipynb
│   ├── classification.ipynb
│   └── clustering.ipynb
│
├── models/
│   └── .gitkeep
│
└── app/
    └── .gitkeep
```

## Machine Learning Tracks

### Regression
- **Dataset**: UNSW-NB15
- **Planned Target**: `sloss` (Source packet loss)
- **Planned Algorithms**:
  1. Linear Regression
  2. Ridge Regression
  3. Lasso Regression
  4. ElasticNet Regression
  5. Polynomial Regression
  6. Decision Tree Regressor
  7. Random Forest Regressor
  8. Gradient Boosting Regressor
  9. Support Vector Regressor
  10. K-Nearest Neighbors Regressor
- **Required Metrics**:
  - Coefficient of Determination ($R^2$)
  - Root Mean Squared Error (RMSE)
  - Mean Absolute Error (MAE)
  - 5-Fold Cross-Validated $R^2$ (evaluated on the top 2 performing models)

### Classification
- **Dataset**: CIC-IDS2017
- **Review 1 — Part A Algorithms**:
  1. Logistic Regression
  2. K-Nearest Neighbors
  3. Gaussian Naive Bayes
  4. Decision Tree Classifier
  5. Support Vector Machine
- **Review 2 — Part B Algorithms**:
  6. Random Forest Classifier
  7. AdaBoost Classifier
  8. Gradient Boosting Classifier
  9. Bagging Classifier
  10. Multi-Layer Perceptron (MLP) Classifier
- **Required Metrics**:
  - Accuracy
  - Precision
  - Recall
  - Weighted $F_1$-score
  - Confusion Matrix
  - ROC-AUC using One-vs-Rest (OvR) for multi-class classification

### Clustering
- **Dataset**: CTU-13
- **Planned Algorithms**:
  1. K-Means Clustering
  2. Agglomerative Hierarchical Clustering
- **Required Metrics**:
  - Silhouette Score
  - Davies-Bouldin Index
  - Calinski-Harabasz Index
- **Required Visualizations**:
  - K-Means Elbow Curve
  - Hierarchical Dendrogram
  - PCA 2D Scatter Visualization
  - t-SNE 2D Projection (where applicable)

## Repository Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/ysujith728/NetGuard-QoS-IDS.git
   cd NetGuard-QoS-IDS
   ```

2. **Create and Activate a Virtual Environment**:
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On Linux/macOS:
   source venv/bin/activate
   ```

3. **Install Required Packages**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Download Datasets**:
   - Download UNSW-NB15 from the official source ([UNSW Research Datasets](https://research.unsw.edu.au/projects/unsw-nb15-dataset)).
   - Download CIC-IDS2017 from the official UNB source ([UNB Canadian Institute for Cybersecurity](https://www.unb.ca/cic/datasets/ids-2017.html)).
   - Download CTU-13 from the official Stratosphere IPS source ([Stratosphere IPS CTU-13](https://www.stratosphereips.org/datasets-ctu13)).

5. **Place Datasets into Local Folders**:
   - Place `UNSW_NB15_training-set.csv` into `data/regression/`.
   - Place CIC-IDS2017 CSV file(s) into `data/classification/`.
   - Place CTU-13 flow CSV file(s) into `data/clustering/`.

6. **Run Jupyter Notebooks**:
   ```bash
   jupyter notebook
   ```
   Navigate to `notebooks/` and open `regression.ipynb`, `classification.ipynb`, or `clustering.ipynb`.

## Results

> Results will be added after model training and evaluation.

## Team

> Team details placeholder (to be updated).

## Academic Integrity

This project is conducted as part of the 23CSE301 Machine Learning Capstone course. All data analysis, feature engineering, model training, interpretation, and visualization are executed independently by the team. External literature, toolkits, libraries, and AI coding assistants are utilized and acknowledged strictly in accordance with course academic integrity guidelines.
