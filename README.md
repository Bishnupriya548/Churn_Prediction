<img width="1357" height="672" alt="image" src="https://github.com/user-attachments/assets/3b927b91-43cf-4d75-8740-8dae57ed1d36" /># Churn_Prediction
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
* **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

## ⚙️ Methodology

### 1. Data Preprocessing
* **Cleaning:** Handled missing values in the `TotalCharges` column by imputing the median.
* **Feature Engineering:** * Dropped irrelevant columns (e.g., `customerID`).
    * Converted `TotalCharges` to numeric type.
* **Encoding:** Applied **One-Hot Encoding** to categorical variables (e.g., Internet Service, Payment Method) and **Label Encoding** to binary variables.
* **Scaling:** Standardized numerical features (`tenure`, `MonthlyCharges`) using `StandardScaler` to ensure the model treats all features equally.

### 2. Model Building
* **Algorithm:** Random Forest Classifier.
* **Why Random Forest?** It was chosen for its ability to handle large datasets with higher dimensionality and its resistance to overfitting compared to Decision Trees.
* **Split:** Data was split into 80% Training and 20% Testing sets.

## 📈 Results & Business Insights

* **Model Accuracy:** ~79%
* **Precision/Recall:** The model successfully identifies the majority of non-churners and significant patterns in churners.

### Key Drivers of Churn:
According to the Feature Importance analysis, the top factors contributing to churn are:
1.  **Contract Type:** Customers with **Month-to-Month** contracts are significantly more likely to leave.
2.  **Tenure:** New customers (low tenure) are at higher risk of leaving early.
3.  **Monthly Charges:** Higher monthly costs correlate with higher churn rates.

## 🖼️ Visualizations
<img width="669" height="579" alt="image" src="https://github.com/user-attachments/assets/ef3dc439-4fb4-48c2-a7dc-daf2f0af0f07" />

<img width="1293" height="665" alt="image" src="https://github.com/user-attachments/assets/23a7910c-ac0a-4a72-a656-1d0c59455529" />

* **Confusion Matrix:** visualizes the True Positives and True Negatives.
* **Feature Importance Plot:** Visualizes which variables impact the prediction most.

## 🔮 Future Improvements
* **Hyperparameter Tuning:** Use GridSearch to optimize the Random Forest parameters (e.g., `max_depth`, `n_estimators`).
* **Handling Class Imbalance:** Implement techniques like SMOTE or Class Weights to further improve recall for the minority class (Churners).

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/Bishnupriya548/churn-prediction.git](https://github.com/Bishnupriya548/churn-prediction.git)
