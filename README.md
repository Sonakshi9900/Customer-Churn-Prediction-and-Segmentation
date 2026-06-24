# 📉 Customer Churn Prediction & Segmentation

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-yellowgreen?logo=scikit-learn&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sonakshi9900/Customer-Churn-Prediction-and-Segmentation/blob/main/CBSOT_project1.ipynb)

> A machine learning project that predicts customer churn and segments customers using the IBM Telco Customer Churn dataset — enabling telecom businesses to proactively retain at-risk customers.

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Business Problem](#-business-problem)
- [Dataset](#-dataset)
- [Project Workflow](#-project-workflow)
- [Key Techniques](#-key-techniques)
- [Results](#-results)
- [Technologies Used](#-technologies-used)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Author](#-author)

---

## 🔍 Overview

Customer churn — when a customer stops using a company's service — is one of the most critical challenges in the telecom industry. Acquiring a new customer costs significantly more than retaining an existing one. This project combines **predictive modeling** and **customer segmentation** to:

- Identify customers most likely to churn
- Understand behavioral patterns across different customer groups
- Provide actionable insights for targeted retention strategies

---

## 💼 Business Problem

Telecom companies face high churn rates, leading to substantial revenue loss. The core questions this project addresses are:

- Which customers are at the highest risk of churning?
- What factors most strongly influence the decision to leave?
- Can we group customers into meaningful segments to tailor retention efforts?

---

## 📊 Dataset

**Source:** IBM Telco Customer Churn Dataset (`Telco_customer_churn.xlsx`)

| Property | Details |
|---|---|
| Records | ~7,043 customers |
| Features | 21 attributes |
| Target | `Churn` (Yes / No) |

**Key Features Include:**
- **Demographics:** Gender, SeniorCitizen, Partner, Dependents
- **Account Info:** Tenure, Contract type, PaperlessBilling, PaymentMethod
- **Services:** PhoneService, InternetService, StreamingTV, TechSupport
- **Financials:** MonthlyCharges, TotalCharges

---

## 🔄 Project Workflow

```
Raw Data
   │
   ▼
Data Loading & Exploration (EDA)
   │
   ▼
Data Preprocessing
(Handle missing values, encode categoricals, scale features)
   │
   ▼
   ├──► Churn Prediction (Classification Models)
   │         └─ Logistic Regression / Random Forest / XGBoost
   │
   └──► Customer Segmentation (Clustering)
             └─ K-Means Clustering
   │
   ▼
Model Evaluation & Insights
   │
   ▼
Business Recommendations
```

---

## 🛠 Key Techniques

### 1. Exploratory Data Analysis (EDA)
- Distribution analysis of churn vs. non-churn customers
- Correlation heatmaps and feature relationships
- Visual insights on tenure, contract type, and monthly charges

### 2. Data Preprocessing
- Handling missing/null values in `TotalCharges`
- Label encoding and one-hot encoding for categorical variables
- Feature scaling using `StandardScaler`
- Train/test split with stratification

### 3. Churn Prediction (Classification)
- **Logistic Regression** — baseline model
- **Random Forest Classifier** — ensemble-based predictions
- **XGBoost / Gradient Boosting** — boosted performance
- Evaluation via Accuracy, Precision, Recall, F1-Score, ROC-AUC

### 4. Customer Segmentation (Clustering)
- **K-Means Clustering** for unsupervised customer grouping
- Elbow method to determine optimal number of clusters
- Segment profiling: high-value, at-risk, loyal, and new customers

---

## 📈 Results

| Model | Accuracy | ROC-AUC |
|---|---|---|
| Logistic Regression | ~80% | ~0.84 |
| Random Forest | ~82% | ~0.87 |
| XGBoost | ~83%+ | ~0.88+ |

**Key Findings:**
- Customers on **month-to-month contracts** churn at significantly higher rates
- **Fiber optic** internet users show higher churn compared to DSL users
- **Senior citizens** and customers without dependents are more likely to churn
- High **monthly charges** combined with short tenure is a strong churn indicator
- Segmentation revealed distinct groups that can be targeted with tailored offers

---

## 🧰 Technologies Used

| Category | Tools / Libraries |
|---|---|
| Language | Python 3.8+ |
| Data Manipulation | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn, XGBoost |
| Clustering | Scikit-learn (KMeans) |
| Environment | Jupyter Notebook |
| Data Format | Excel (`.xlsx`) |

---

## 🚀 Getting Started

### ▶️ Run Directly in Google Colab (No Setup Required)

Click the badge below to open and run the notebook instantly in your browser:

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sonakshi9900/Customer-Churn-Prediction-and-Segmentation/blob/main/CBSOT_project1.ipynb)

> **Note:** After opening in Colab, upload `Telco_customer_churn.xlsx` manually using:
> ```python
> from google.colab import files
> uploaded = files.upload()
> ```

---

### 💻 Run Locally

### Prerequisites

```bash
Python 3.8+
pip
```

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/Sonakshi9900/Customer-Churn-Prediction-and-Segmentation.git
cd Customer-Churn-Prediction-and-Segmentation

# 2. Install required libraries
pip install pandas numpy matplotlib seaborn scikit-learn xgboost openpyxl jupyter

# 3. Launch Jupyter Notebook
jupyter notebook CBSOT_project1.ipynb
```

---

## 📁 Project Structure

```
Customer-Churn-Prediction-and-Segmentation/
│
├── CBSOT_project1.ipynb        # Main analysis notebook
├── Telco_customer_churn.xlsx   # Dataset
└── README.md                   # Project documentation
```

---

## 👩‍💻 Author

**Sonakshi**

[![GitHub](https://img.shields.io/badge/GitHub-Sonakshi9900-black?logo=github)](https://github.com/Sonakshi9900)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

> ⭐ If you found this project helpful, please consider giving it a star!
