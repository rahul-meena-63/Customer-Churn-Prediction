 ## 📊 Customer Churn Analysis & Prediction Dashboard

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://cusomer-churn-predictor.streamlit.app/)
![Python](https://img.shields.io/badge/Python-Data%20Analysis-blue)
![SQL](https://img.shields.io/badge/SQL-SQLite3-lightgrey)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--learn-orange)
![Dashboard](https://img.shields.io/badge/Dashboard-Streamlit-red)

**🚀 Live Interactive Dashboard:** [Open Customer Churn Dashboard](https://cusomer-churn-predictor.streamlit.app/)

---

## 🎯 Project Overview

- End-to-end data analytics and machine learning project focused on customer churn in a telecom subscription business.
- Uses the IBM customer churn dataset containing **7,043 customer records and 21 columns**.
- Converts raw customer data into business insights through:
  - Data cleaning and preparation.
  - Exploratory Data Analysis (EDA).
  - SQL-based business analysis.
  - Machine learning and churn prediction.
  - Interactive Streamlit dashboard.
- Focuses on understanding why customers leave and identifying customers who may leave in the future.

## 🚀 Business Problem & Objective

- **Business Problem:** Customer churn reduces recurring revenue and makes customer retention difficult for subscription-based businesses.
- **Project Objective:** Understand customer churn, identify the factors associated with it, predict potential churn, and recommend actions to improve customer retention.
- **Key Business Questions:**
  1. How many customers are leaving the company?
  2. Which customer characteristics and services are associated with churn?
  3. Can machine learning identify customers who may leave?
  4. What actions can the business take to reduce customer churn?

---

## ✨ Features & Key Insights

- 📊 **Customer Churn Analysis:** Measures the overall churn rate and identifies patterns in customer behavior.
- 🧹 **Data Cleaning & Preparation:** Handles missing values and prepares the customer dataset for analysis and modeling.
- 🔎 **Exploratory Data Analysis (EDA):** Uses charts and visualizations to explore customer segments and churn patterns.
- 🗄️ **SQL Business Analysis:** Analyzes churn by contract type, payment method, customer segment, cohort, and revenue.
- 🤖 **Machine Learning:** Trains and compares Logistic Regression, Decision Tree, and Random Forest classifiers.
- 📈 **Model Evaluation:** Compares model performance using accuracy, precision, recall, F1-score, and ROC-AUC.
- 🖥️ **Interactive Dashboard:** Provides a Streamlit interface for customer churn analysis and risk prediction.
- 💡 **Business Recommendations:** Converts analytical findings into customer retention strategies.

### 📌 Key Business Findings

| Business Metric | Result |
|---|---:|
| Total Customers | 7,043 |
| Customers Who Churned | 1,869 |
| Overall Churn Rate | **26.54%** |
| Monthly Charges Associated with Churned Customers | **$139,130.85** |

### 📃 Contract Type Analysis

| Contract Type | Churn Rate |
|---|---:|
| Month-to-month | **42.71%** |
| One year | 11.27% |
| Two year | 2.83% |

- Month-to-month customers have the highest churn rate.
- Customers with longer-term contracts have lower churn rates.

### 💳 Payment Method Analysis

| Payment Method | Churn Rate |
|---|---:|
| Electronic check | **45.29%** |
| Automatic credit card | 15.24% |
| Automatic bank transfer | 16.71% |

- Electronic check users show the highest churn rate among the listed payment methods.
- Automatic payment users show lower churn rates in this analysis.

### ⚠️ High-Risk Customer Segment

- **Customer Segment:** Month-to-month contract + Fiber Optic internet + Electronic check payment.
- **Churn Rate:** **60.37%**
- **Customers in Segment:** 1,307
- **Customers Who Churned:** 789

---

## 🛠 Tech Stack & Architecture

| Layer / Stage | Technology | Official Link | Architectural Role |
| :--- | :--- | :--- | :--- |
| **Data Analysis & Cleaning** | NumPy, Pandas | [numpy.org](https://numpy.org/), [pandas.pydata.org](https://pandas.pydata.org/)| Data analysis and model development  |
| **Data Visualization** | Matplotlib, Seaborn, Plotly | [matplotlib.org](https://matplotlib.org/), [seaborn.pydata.org](https://seaborn.pydata.org/), [plotly.com/python](https://plotly.com/python/)  | Train and evaluate churn prediction models |  
| **Machine Learning** | Scikit-Learn (Logistic Regression, Decision Tree, Random Forest) | [scikit-learn.org](https://scikit-learn.org/) | Applied machine learning algorythm and compare with other algorithyms   |
| **Dashboard & UI** | Streamlit | [streamlit.io](https://streamlit.io/) | Build the interactive web application |


## 🗂️ Project Structure

```text
customer-churn-analytics/
├── .gitignore
├── README.md
├── requirements.txt
│
├── data/
│   ├── raw/
│   │   └── WA_Fn-UseC_-Telco-Customer-Churn.csv
│   └── processed/
│       └── customer_churn_cleaned.csv
│
├── database/
│   ├── churn.db                     # SQLite database file
│   ├── schema.sql                   # Table creation script
│   └── queries.sql                  # Analytical SQL queries (SQLite & T-SQL)
│
├── notebooks/
│   ├── 01_eda_data_cleaning.ipynb   # Exploratory Data Analysis
│   └── 02_model_training.ipynb      # ML feature engineering & training
│
├── models/
│   └── churn_prediction.pkl         # Serialized trained model
│
├── powerbi/
│   ├── customer_churn_dashboard.pbix
│   └── dax_measures.txt             # Documented DAX formulas
│
├── src/
│   ├── __init__.py
│   ├── db_connection.py             # SQLite / MS SQL Server connection logic
│   └── predict.py                   # Model inference helpers
│
└── app.py                           # Streamlit dashboard application

```

### 📁 Repository Structure

All core files are listed below with clickable links for instant inspection:

* 📁 **data/** - Contains the database setup and data storage
  * 📄 **customer_churn.csv** - The raw IBM customer churn dataset (7,043 rows, 21 columns)
  * 📄 **customer_churn_cleaned.csv** - Cleaned, preprocessed dataset ready for modeling and dashboarding
  * 📄 **db_setup.py** - Python script that cleans data, handles missing values, and populates SQLite
  * 🗄️ **churn.db** - SQLite database containing the final `customers` table
* 📁 **notebooks/** - Jupyter exploratory notebooks
  * 📓 **EDA.ipynb** - Pre-run Jupyter Notebook containing all data cleaning notes, plots, and business insights
* 📁 **sql/** - Analytical database queries
  * 📄 **churn_analysis.sql** - Business intelligence queries answering contract, segment, cohort, and revenue churn questions
* 📁 **model/** - Machine Learning assets
  * 📄 **train.py** - Python script that trains Logistic Regression, Decision Tree, and Random Forest models, prints results, and serializes the best estimator
  * 💾 **churn_prediction.pkl** - Best trained Random Forest prediction pipeline pickle file
* 💻 **app.py** - The interactive Streamlit dashboard and risk predictor application
---

## 🗄️ Database Schema & SQL Buainess Insights

- Customer data is stored in an SQLite database.
- The main database table is named **`customers`**.
- Key columns used in the analysis are listed below.

| Column | Data Type | Description |
|---|---|---|
| `customer_id` | `VARCHAR(50)` (PK) | Unique identifier for each customer |
| `gender` | `VARCHAR(10)` | Male / Female |
| `senior_citizen` | `INTEGER` | 1 if senior citizen, 0 if not |
| `tenure` | `INTEGER` | Number of months the customer has stayed with the company |
| `contract` | `VARCHAR(20)` | Month-to-month, One year, or Two year |
| `monthly_charges` | `REAL` | Current monthly bill amount |
| `total_charges` | `REAL` | Total amount billed to date |
| `churn` | `VARCHAR(5)` | Target field: Yes (customer left) or No (customer stayed) |
| `payment_method` | `VARCHAR(30)` | Electronic check, Mailed check, Automatic card, or Automatic bank |
| `internet_service` | `VARCHAR(20)` | Fiber optic, DSL, or None |
| `tech_support` | `VARCHAR(20)` | Yes, No, or No internet service |

---

### 🤖 Machine Learning Algorithms

- Logistic Regression
- Decision Tree
- Random Forest

### 📊 Model Performance Comparison

- Models were evaluated using a **20% holdout test set**.
- Numerical features were processed using Standard Scaling.
- Categorical features were processed using One-Hot Encoding.

| Model | Test Accuracy | Test Precision | Test Recall | Test F1-Score | Test ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 80.70% | 66.04% | **56.15%** | **60.69%** | 84.22% |
| Decision Tree | 79.42% | 63.12% | 54.01% | 58.21% | 82.67% |
| Random Forest | **80.34%** | **67.64%** | 49.73% | 57.32% | **84.27%** |

### 🏆 Model Selection

- Random Forest achieved the highest ROC-AUC score: **84.27%**.
- Random Forest was selected as the final prediction pipeline and saved as `model/churn_prediction.pkl`.
- Logistic Regression achieved the highest recall and F1-score among the three models.
- Random Forest achieved the highest precision and ROC-AUC.
- Model selection is based on ROC-AUC in this project; the most suitable model may differ depending on the business objective.

### 🔍 Logistic Regression – Odds-Ratio Analysis

| Factor | Odds Ratio | Interpretation |
|---|---:|---|
| Fiber Optic Internet | 3.26 | Associated with 226% higher odds of churn |
| Electronic Check Payment | 1.47 | Associated with 47% higher odds of churn |
| Two-Year Contract | 0.27 | Associated with 73% lower odds of churn |
| Tenure | 0.29 | Associated with 71% lower odds of churn per standard unit |

- Odds ratios describe changes in **odds**, not direct percentage-point changes in churn probability.
- The tenure interpretation is based on one standardized unit.

## 🖥️ Interactive Streamlit Dashboard

- **Live Application:** [Customer Churn Prediction Dashboard](https://cusomer-churn-predictor.streamlit.app/)
- Built using Streamlit.
- Brings the project's analysis and customer risk prediction functionality together in one web application.
- Allows users to explore the project's churn analysis and use its customer risk prediction application.

---

## ⚙️ How to Run the Project Locally

### 1. Requirements

- Install **Python 3.8 or later**.
- Install the required Python libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn streamlit plotly nbformat nbconvert
```

### 2. Run Data Cleaning & Database Setup

- Run the data preparation script:

```bash
python3 data/db_setup.py
```

- This script:
  - Cleans the raw customer data.
  - Handles missing values.
  - Loads the prepared customer data into the SQLite database.

### 3. Run Machine Learning Model Training

- Run the training script:

```bash
python3 model/train.py
```

- This script:
  - Trains Logistic Regression, Decision Tree, and Random Forest models.
  - Evaluates model performance.
  - Prints the evaluation metrics.
  - Saves the selected prediction pipeline.

### 4. Launch the Streamlit Dashboard

- Start the application locally:

```bash
streamlit run app.py
```

- Or open the deployed dashboard:

[https://cusomer-churn-predictor.streamlit.app/](https://cusomer-churn-predictor.streamlit.app/)

---

## 💡 Business Recommendations & Retention Strategies

### 1. 📃 Encourage Customers to Choose Longer Contracts

- **Insight:**
  - Month-to-month customers represent **88% of all churned accounts**.
- **Action:**
  - Run targeted email and SMS campaigns for month-to-month customers.
  - Offer a **$10/month contract credit** when customers upgrade to a 12-month commitment.
- **Business Goal:**
  - Encourage longer customer commitments and reduce churn among month-to-month subscribers.

### 2. 💳 Encourage Automatic Payment Enrollment

- **Insight:**
  - Electronic check users have the highest churn rate at approximately **45.3%**.
- **Action:**
  - Offer a one-time **$15 account credit** to customers who enroll in Auto-Pay using a credit card or bank transfer.
- **Business Goal:**
  - Encourage automatic payments and reduce reliance on manual electronic checks.

### 3. 👋 Improve the First Six Months of the Customer Journey

- **Insight:**
  - More than **52.9% of new customer churn happens within the first six months**.
- **Action:**
  - Introduce an early customer engagement program:
    - **Month 1:** Welcome email and onboarding support.
    - **Month 3:** Customer satisfaction check-in.
    - **Month 5:** Feedback call and additional support.
- **Business Goal:**
  - Identify customer issues early and improve the experience of new subscribers.

### 4. 🔐 Bundle Security & Technical Support Services

- **Insight:**
  - Customers without Online Security or Tech Support have a churn rate of approximately **49%**.
  - Customers with both services have a churn rate of **9.0%**.
- **Action:**
  - Bundle security and technical support features into premium fiber-optic internet packages instead of selling them only as separate add-ons.
- **Business Goal:**
  - Increase customer value and support better customer retention.

---

## ✅ Project Conclusion

- Analyzed customer churn using Python, SQL, and data visualization tools.
- Identified an overall churn rate of **26.54%** across 7,043 customers.
- Identified **$139,130.85 in monthly charges associated with churned customers**.
- Found important churn patterns related to contract type, payment method, tenure, and services.
- Built and compared three machine learning classification models.
- Selected Random Forest based on its highest ROC-AUC score of **84.27%**.
- Developed an interactive Streamlit dashboard for churn analysis and customer risk prediction.
- Proposed four data-driven retention strategies to help reduce customer loss and protect recurring revenue.

**⭐ Project Outcome:** Transforms raw customer data into clear business insights, churn predictions, and practical customer retention recommendations.
