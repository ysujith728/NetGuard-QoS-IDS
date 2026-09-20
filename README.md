<div align="center">

# 🛡️ NetGuard-QoS-IDS

### NetGuard: QoS-Aware Network Intrusion Detection Using Comparative Machine Learning

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Lab-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Course](https://img.shields.io/badge/Capstone-23CSE301-purple?style=for-the-badge)](https://github.com/ysujith728/NetGuard-QoS-IDS)

---

</div>

## 📌 Overview

**NetGuard-QoS-IDS** is a B.Tech CSE (**23CSE301 Machine Learning Capstone**) project that performs comparative machine-learning analysis across three independent tracks:

* 📉 **Regression** — Predicting continuous network QoS and traffic degradation metrics.
* 🛡️ **Classification** — Classifying network attacks and intrusion activities into discrete attack categories.
* 🔍 **Clustering** — Unsupervised grouping and structural analysis of network traffic behaviour.

Each machine learning track is conducted independently using a separate, dedicated dataset:
* **Regression Track**: UNSW-NB15 dataset
* **Classification Track**: CIC-IDS2017 dataset
* **Clustering Track**: CTU-13 dataset

---

## 🎯 Problem Statement

Modern network infrastructures require automated, machine-learning-driven monitoring to maintain Quality of Service (QoS) and defend against malicious cyber threats. This capstone project addresses three core operational challenges in network traffic analysis:

* 📊 **QoS & Traffic Degradation Prediction**: Estimating continuous performance indicators (such as packet loss or latency metrics) from flow characteristics to proactively optimize network resources.
* 🛡️ **Network Intrusion Classification**: Accurately distinguishing benign traffic from diverse attack vectors (e.g., DoS, Port Scans, Brute Force, Malware) across multi-class scenarios.
* 🧩 **Unsupervised Traffic Behaviour Profiling**: Discovering hidden traffic structures, anomaly patterns, and operational clusters without prior label annotations.

---

## 📊 Datasets

| Track | Dataset | Purpose |
| :--- | :--- | :--- |
| **Regression** | **UNSW-NB15** | Network traffic / QoS regression |
| **Classification** | **CIC-IDS2017** | Network attack classification |
| **Clustering** | **CTU-13** | Unsupervised network traffic behaviour analysis |

> [!NOTE]
> The raw regression dataset (`UNSW_NB15_training-set.csv`) and classification dataset (`network_traffic_classification.csv`, via Git LFS) are tracked in the repository for these project milestones.

---

## 📁 Project Structure

```text
NetGuard-QoS-IDS/
│
├── README.md
├── requirements.txt
├── .gitignore
├── .gitattributes
│
├── data/
│   ├── regression/
│   │   ├── UNSW_NB15_training-set.csv
│   │   └── README.md
│   │
│   ├── classification/
│   │   ├── network_traffic_classification.csv (Git LFS)
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

---

## 🤖 Machine Learning Tracks

### 📈 Regression
* **Dataset**: UNSW-NB15
* **Planned Target**: `sloss` (Source packet loss)
* **Planned Algorithms**:
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
* **Required Metrics**:
  * Coefficient of Determination ($R^2$)
  * Root Mean Squared Error (RMSE)
  * Mean Absolute Error (MAE)
  * 5-Fold Cross-Validated $R^2$ (evaluated on the top 2 performing models)

---

### 🛡️ Classification
* **Dataset**: CIC-IDS2017
* **Review 1 — Part A Algorithms**:
  1. Logistic Regression
  2. K-Nearest Neighbors
  3. Gaussian Naive Bayes
  4. Decision Tree Classifier
  5. Support Vector Machine
* **Review 2 — Part B Algorithms**:
  6. Random Forest Classifier
  7. AdaBoost Classifier
  8. Gradient Boosting Classifier
  9. Bagging Classifier
  10. Multi-Layer Perceptron (MLP) Classifier
* **Required Metrics**:
  * Accuracy
  * Precision
  * Recall
  * Weighted $F_1$-score
  * Confusion Matrix
  * ROC-AUC using One-vs-Rest (OvR) for multi-class classification

---

### 🔍 Clustering
* **Dataset**: CTU-13
* **Planned Algorithms**:
  1. K-Means Clustering
  2. Agglomerative Hierarchical Clustering
* **Required Metrics**:
  * Silhouette Score
  * Davies-Bouldin Index
  * Calinski-Harabasz Index
* **Required Visualizations**:
  * K-Means Elbow Curve
  * Hierarchical Dendrogram
  * PCA 2D Scatter Visualization
  * t-SNE 2D Projection (where applicable)

---

## 🚀 Repository Setup

### 1. Clone the Repository
```bash
git clone https://github.com/ysujith728/NetGuard-QoS-IDS.git
cd NetGuard-QoS-IDS
```

### 2. Create and Activate a Virtual Environment
```bash
python -m venv venv

# On Windows:
venv\Scripts\activate

# On Linux/macOS:
source venv/bin/activate
```

### 3. Install Required Packages
```bash
pip install -r requirements.txt
```

### 4. Download Datasets
* Download **UNSW-NB15** from the official source ([UNSW Research Datasets](https://research.unsw.edu.au/projects/unsw-nb15-dataset)).
* Download **CIC-IDS2017** from the official UNB source ([UNB Canadian Institute for Cybersecurity](https://www.unb.ca/cic/datasets/ids-2017.html)).
* Download **CTU-13** from the official Stratosphere IPS source ([Stratosphere IPS CTU-13](https://www.stratosphereips.org/datasets-ctu13)).

### 5. Place Datasets into Local Folders
* Place `UNSW_NB15_training-set.csv` into `data/regression/`.
* Place CIC-IDS2017 CSV file(s) into `data/classification/`.
* Place CTU-13 flow CSV file(s) into `data/clustering/`.

### 6. Run Jupyter Notebooks
```bash
jupyter notebook
```
Navigate to `notebooks/` and open `regression.ipynb`, `classification.ipynb`, or `clustering.ipynb`.

---

## 📈 Results

### 1. 📉 Regression Performance (UNSW-NB15 — Target: `sloss`)

Comparative performance across all 10 evaluated regression models (including tuned variants and 5-fold cross-validation on top performers):

| Model | $R^2$ Score | 5-Fold CV $R^2$ | RMSE | MAE |
| :--- | :--- | :--- | :--- | :--- |
| **Random Forest Regressor** | **0.999669** | 0.999087 | **1.3914** | 0.0683 |
| **Tuned Random Forest** | 0.999657 | 0.999075 | 1.4158 | **0.0586** |
| **Gradient Boosting Regressor** | 0.999635 | — | 1.4611 | 0.1696 |
| **Tuned Gradient Boosting** | 0.999623 | **0.999170** | 1.4850 | 0.1041 |
| **K-Nearest Neighbors Regressor** | 0.999281 | — | 2.0504 | 0.2836 |
| **Decision Tree Regressor** | 0.999179 | 0.998162 | 2.1914 | 0.0684 |
| **Polynomial Regression** | 0.999128 | — | 2.2588 | 0.5975 |
| **Ridge Regression** | 0.997720 | 0.996843 | 3.6524 | 0.8527 |
| **Linear Regression** | 0.997717 | 0.996840 | 3.6551 | 0.8528 |
| **Lasso Regression** | 0.997660 | — | 3.7002 | 0.7364 |
| **Support Vector Regressor** | 0.997598 | — | 3.7487 | 0.5067 |
| **ElasticNet** | 0.996296 | — | 4.6553 | 1.1955 |

* **Best Overall Regressor**: **Random Forest** achieved the lowest RMSE (`1.3914`) and highest test $R^2$ (`0.999669`), with **Tuned Gradient Boosting** demonstrating the best cross-validated generalization ($R^2 = 0.999170$).

---

### 2. 🛡️ Classification Performance (CIC-IDS2017 — Review 1 Part-A)

Evaluation of the 5 baseline multi-class network intrusion classifiers on held-out test data:

| Algorithm | Model Type | Track Lead | Test Accuracy | Weighted $F_1$-Score |
| :--- | :--- | :--- | :--- | :--- |
| **Logistic Regression** | Linear (Softmax Log-Odds) | Member 1 | **89.69%** (0.896875) | **0.864210** |
| **Support Vector Machine (SVC)** | Maximum-Margin Hyperplane (Linear) | Member 3 | **89.63%** (0.896250) | 0.863017 |
| **Decision Tree Classifier** | Tree-Based (`max_depth=10`) | Member 2 | 88.81% (0.888125) | 0.860935 |
| **K-Nearest Neighbors (KNN)** | Instance-Based ($k=5$) | Member 1 | 87.06% (0.870625) | 0.849195 |
| **Gaussian Naive Bayes** | Probabilistic (Gaussian Prior) | Member 2 | 79.38% (0.793750) | 0.808519 |

* **Top Performers**: **Logistic Regression** and **Linear SVC** yielded the highest accuracy (~89.69%) and weighted $F_1$ scores (~0.8642), offering strong discriminative capability across benign traffic and multi-class intrusion types.

---

### 3. 🔍 Clustering Performance (CTU-13 — Review 2)

> [!NOTE]
> Clustering experiments (K-Means, Agglomerative Hierarchical, PCA/t-SNE visualization) are scheduled for the next review milestone.

---

## 👥 Team

| Member | Name | Roll Number |
| :--- | :--- | :--- |
| **Member 1** | Sujith | `CB.SC.U4CSE24260` |
| **Member 2** | Bhavith | `CB.SC.U4CSE2441` |
| **Member 3** | Vignesh | `CB.SC.U4CSE24265` |

---

## 🎓 Academic Integrity

This project is conducted as part of the **23CSE301 Machine Learning Capstone** course. All data analysis, feature engineering, model training, interpretation, and visualization are executed independently by the team. External literature, toolkits, libraries, and AI coding assistants are utilized and acknowledged strictly in accordance with course academic integrity guidelines.

