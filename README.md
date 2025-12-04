# Churn_Prediction
# 📉 Telco Customer Churn Prediction

## 📌 Project Overview
Customer retention is critical in the telecommunications industry. This project aims to identify customers who are likely to cancel their contracts ("churn") soon. By analyzing customer demographics, services, and billing patterns, this machine learning model predicts churn probability, allowing companies to proactively offer incentives to retain valuable customers.

## 📊 Dataset
The dataset used is the **Telco Customer Churn** dataset from Kaggle.
* **Rows:** 7,043 customers
* **Features:** 21 (including Tenure, Monthly Charges, Payment Method, Contract Type, etc.)
* **Target:** Churn (Yes/No)

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Imbalanced-learn (SMOTE)

## ⚙️ Methodology

### 1. Data Preprocessing
* **Cleaning:** Handled missing values in the `TotalCharges` column by imputing the median.
* **Encoding:** Applied One-Hot Encoding to categorical variables (e.g., Internet Service, Payment Method) and Label Encoding to binary variables.
* **Scaling:** Standardized numerical features (`tenure`, `MonthlyCharges`) using `StandardScaler` to bring them to a common scale.

### 2. Handling Imbalance (Critical Step)
The dataset was highly imbalanced (73% non-churn vs. 27% churn).
* **Solution:** Applied **SMOTE (Synthetic Minority Over-sampling Technique)** on the training set.
* **Result:** Balanced the class distribution, ensuring the model didn't just bias toward the majority class.

### 3. Model Building
* Used **Random Forest Classifier** for its ability to handle non-linear relationships and provide feature importance.
* Split data into 80% Training and 20% Testing sets.

## 📈 Results & Business Insights
* **Model Accuracy:** ~82%
* **F1-Score:** ~0.80

### Key Drivers of Churn:
According to the Feature Importance analysis, the top factors contributing to churn are:
1.  **Contract Type:** Customers with **Month-to-Month** contracts are significantly more likely to leave.
2.  **Tenure:** New customers (low tenure) are at higher risk.
3.  **Internet Service:** Users with **Fiber Optic** internet showed higher churn rates (possibly due to cost or technical issues).

## 🖼️ Visualizations
*(Upload your graphs here)*
* **Confusion Matrix:** Shows the balance between False Positives and False Negatives.
* **Feature Importance Plot:** Visualizes which variables impact the prediction most.

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/yourusername/churn-prediction.git](https://github.com/yourusername/churn-prediction.git)
