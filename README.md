# 🛡️ Credit Card Fraud Detection Pipeline

![Python](https://img.shields.io/badge/Python-3.13-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange.svg)
![Machine Learning](https://img.shields.io/badge/Focus-Fraud_Detection-green.svg)

## 📌 Project Overview
This project focuses on identifying fraudulent credit card transactions using machine learning. The primary challenge addressed is the **extreme class imbalance**, where fraudulent transactions represent only **0.17%** of the total dataset.

The goal was to build a model that maximizes **Recall** (catching as many frauds as possible) while maintaining a low **False Positive Rate** to ensure a smooth experience for legitimate customers.

---

## 🛠️ Technical Stack & Workflow

1. **Environment & Governance:** Isolated development using a Python Virtual Environment (`venv`) for reproducibility.
2. **Data Preprocessing:** - Feature Scaling using `StandardScaler` for 'Amount' and 'Time'.
   - Dimensionality reduction features (V1-V28) handled via PCA-transformed inputs.
3. **Imbalance Handling:** Applied **SMOTE** (Synthetic Minority Over-sampling Technique) to balance the training classes (50/50 split).
4. **Model Architecture:** Utilized **Random Forest Classifier** for its robustness against overfitting and ability to handle non-linear patterns.
5. **Optimization:** Conducted **Hyperparameter Tuning** via `GridSearchCV` focusing on the `Recall` metric.

---

## 📊 Performance Audit

After rigorous tuning and testing on unseen data, the model achieved the following results:

| Metric | Score | Impact |
| :--- | :--- | :--- |
| **Accuracy** | 100% | Overall system stability. |
| **Recall (Class 1)** | **82%** | Successfully caught 80 out of 98 fraud cases. |
| **Precision (Class 1)** | **82%** | High confidence in fraud alerts, reducing "cry wolf" scenarios. |
| **False Positives** | **17** | Only 17 out of 56,864 genuine transactions were flagged (0.03%). |

> **Key Insight:** The model provides a high-confidence security layer, catching 4 out of every 5 frauds without bothering 99.9% of the bank's honest customers.

---

## 📁 Project Structure
- `notebooks/`: Contains the full EDA, training, and GridSearchCV process.
- `models/`: Exported `.pkl` files for the trained model and scaler.
- `requirements.txt`: List of dependencies to recreate the environment.
- `data/`: (Not uploaded due to size) Source: Kaggle Credit Card Fraud Detection dataset.

---

## 🚀 How to Run
1. Clone the repository.
2. Install dependencies: `pip install -r requirements.txt`.
3. Open the Jupyter Notebook to view the analysis or use `joblib.load()` to run the pre-trained model on new data.

---
**Author:** [Your Name]  
**Field:** Data Science / Financial Risk Audit
