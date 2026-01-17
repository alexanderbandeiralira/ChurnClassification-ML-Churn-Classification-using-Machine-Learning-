# 📉 Telco Customer Churn Prediction

![Python](https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-F7931E?style=for-the-badge&logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-Analysis-green?style=for-the-badge)

## 📌 Overview

This project aims to develop a Machine Learning model capable of predicting **Churn (cancellation)** for customers of a telecommunications company.

Identifying customers with a high probability of cancellation allows the company to take preventive retention actions, reducing financial losses and increasing customer satisfaction.

---

## 🗂️ The Dataset

The **Telco Customer Churn** dataset was used, containing information about:
* **Demographics:** Gender, Seniors, Partners, Dependents.
* **Services:** Phone, Internet (DSL/Fiber optic), Online Security, Backup, Streaming, etc.
* **Account:** Contract type, Payment method, Paperless billing.
* **Metrics:** `Tenure` (months with the company), `MonthlyCharges`, `TotalCharges`.
* **Target:** `Churn` (Yes/No).

---

## 📊 Exploratory Data Analysis (EDA)

The initial analysis revealed important patterns in customer behavior.

### 1. Class Imbalance
The dataset presents a natural imbalance, with more retained customers ("No") than cancelled ones ("Yes").

![Churn Distribution](assets/churn_distribution.png)

### 2. Feature Correlation
We investigated how numerical variables (such as monthly charges and tenure) relate to cancellation.

**Key Insights:**
* Customers with **month-to-month contracts** have a higher cancellation rate.
* New customers (low `tenure`) are more prone to churn.
* **Fiber Optic** users show higher churn rates than DSL users.

---

## ⚙️ Machine Learning Pipeline

The project followed a rigorous data processing workflow:

1.  **Preprocessing:**
    * Handling missing values in `TotalCharges`.
    * Converting the target variable (`Churn`) to binary (0/1).
    * **Encoding:** Used `Get Dummies` for categorical variables.
    * **Scaling:** Normalization of numerical data using `MinMaxScaler`.
2.  **Modeling:**
    * Several algorithms were tested, including:
    * Logistic Regression
    * Decision Tree
    * Random Forest
    * **Gradient Boosting (Chosen Model)**
    * XGBoost / LGBM

---

## 🏆 Results

The **Gradient Boosting** model showed the best overall performance, balancing generalization capability and precision in detecting cancellations.

### Confusion Matrix
Below is the model's performance on the test data:

![Confusion Matrix](assets/confusion_matrix.png)

| Metric | Performance |
| :--- | :---: |
| **Accuracy** | **~80%** |
| **Precision** | **High** |
| **Recall** | **Balanced** |

*The model proved effective for segmenting the customer base and prioritizing marketing actions.*

---

## 🚀 How to Run

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/alexanderbandeiralira/ChurnClassification-ML-Churn-Classification-using-Machine-Learning-](https://github.com/alexanderbandeiralira/ChurnClassification-ML-Churn-Classification-using-Machine-Learning-)
    ```
2.  **Install dependencies:**
    ```bash
    pip install pandas numpy scikit-learn seaborn matplotlib plotly xgboost lightgbm
    ```
3.  **Run the Notebook:**
    Open the `Churn_Analysis_Telco.ipynb` file in Jupyter or Google Colab.

---

## 👨‍💻 Author

**Alexander Lira**
*Data Scientist | Machine Learning*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/alexanderblira/)
