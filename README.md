# 💳 Machine Learning Based Fraudulent Transaction Detection System

A Machine Learning-based system developed to detect fraudulent credit card transactions using supervised learning algorithms. The project evaluates multiple machine learning models and deploys the best-performing model to classify unseen transactions as **Legitimate** or **Fraudulent**.

> **Academic Project:** Master of Computer Applications (MCA) – Minor Project

---

## 📌 Project Overview

With the rapid growth of digital payment systems, detecting fraudulent financial transactions has become a major challenge for financial institutions. Traditional rule-based systems often fail to identify evolving fraud patterns.

This project proposes a **Machine Learning-Based Fraudulent Transaction Detection System** that:

- Performs data quality assessment and preprocessing.
- Handles severe class imbalance using **SMOTE**.
- Trains and compares multiple machine learning algorithms.
- Selects the best-performing model.
- Predicts whether unseen transactions are fraudulent or legitimate.

---

## 🎯 Objectives

- Develop a fraud detection system using supervised machine learning.
- Compare the performance of multiple classification algorithms.
- Handle highly imbalanced transaction data.
- Evaluate models using appropriate performance metrics.
- Deploy the best model for fraud prediction.

---

## 🏗️ System Architecture

```text
                    Credit Card Dataset
                            │
                            ▼
               Data Quality Assessment
                            │
                            ▼
            Exploratory Data Analysis (EDA)
                            │
                            ▼
                  Data Preprocessing
      (Duplicate Removal, Scaling, SMOTE)
                            │
                            ▼
               Machine Learning Models
        ┌────────────┬────────────┬──────────────┬─────────────┐
        │ Logistic   │ Decision   │ Random       │ XGBoost     │
        │ Regression │ Tree       │ Forest       │             │
        └────────────┴────────────┴──────────────┴─────────────┘
                            │
                            ▼
                 Model Performance Comparison
                            │
                            ▼
              Best Model (Random Forest)
                            │
                            ▼
          Fraud Prediction on New Transactions
```

---

## 📂 Project Structure

```text
Fraud-Detection-System/
│
├── data/
│   └── raw/
│       └── creditcard.csv
│
├── models/
│   ├── random_forest_model.pkl
│   └── scaler.pkl
│
├── notebooks/
│   └── Fraud_Detection.ipynb
│
├── outputs/
│   ├── figures/
│   ├── model_comparison.csv
│   └── sample_predictions.csv
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 🛠️ Technologies Used

- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Imbalanced-learn (SMOTE)
- Joblib
- Jupyter Notebook
- Visual Studio Code
- Git & GitHub

---

## 📊 Dataset

The project uses the **Credit Card Fraud Detection Dataset** made publicly available on Kaggle.

**Dataset Source:**

https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Place the downloaded `creditcard.csv` file inside:

```text
data/raw/
```

---

## ⚙️ Installation

### Clone the repository

```bash
git clone <repository-url>
cd Fraud-Detection-System
```

### Create a virtual environment

```bash
python -m venv .venv
```

### Activate the environment

**Windows**

```bash
.venv\Scripts\activate
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
notebooks/Fraud_Detection.ipynb
```

---

## 🤖 Machine Learning Models

The following supervised learning algorithms were implemented and compared:

- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost

---

## 📈 Model Evaluation Metrics

Each model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score
- Confusion Matrix

---

## 🏆 Model Performance

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|------|---------:|----------:|--------:|---------:|---------:|
| Logistic Regression | 97.37% | 5.30% | **87.37%** | 10.00% | 96.26% |
| Decision Tree | 99.74% | 35.26% | 64.21% | 45.52% | 82.01% |
| **Random Forest** ⭐ | **99.95%** | **91.25%** | 76.84% | **83.43%** | 96.94% |
| XGBoost | 99.92% | 74.26% | **78.95%** | 76.53% | **97.02%** |

**Selected Model:** Random Forest

---

## 🔍 Fraud Detection Module

The trained Random Forest model is saved using **Joblib** and reused to classify unseen transactions.

The system outputs:

- Transaction Classification
  - Legitimate
  - Fraudulent
- Fraud Probability
- Prediction Validation

---

## 🚀 Future Enhancements

- Develop a web application using Flask or Streamlit.
- Integrate real-time transaction monitoring.
- Deploy the model using REST APIs.
- Explore deep learning techniques for fraud detection.
- Implement real-time alert notifications.

---

## 👩‍💻 Author

**Rija Mary Jacob**

Master of Computer Applications (MCA)

---

## 📄 License

This repository is intended for academic and educational purposes.