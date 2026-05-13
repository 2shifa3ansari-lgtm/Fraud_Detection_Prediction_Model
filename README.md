# Fraud_Detection_Prediction_Model
A machine learning project that identifies fraudulent transactions using classification algorithms and performance evaluation techniques.

# Financial Fraud Detection Prediction Model

## 📌 Project Overview
This project focuses on detecting fraudulent financial transactions using **Machine Learning** and **Exploratory Data Analysis (EDA)**. The model analyzes transaction patterns, balances, amounts, and transaction types to identify potentially fraudulent activities.

Financial fraud has become a major challenge in digital transactions. This project aims to build an intelligent fraud detection system that can help reduce risks by predicting suspicious transactions.

---

## 🎯 Objectives
- Analyze transaction data to identify fraud patterns.
- Perform data preprocessing and feature engineering.
- Visualize transaction trends and fraud behavior.
- Build a machine learning model for fraud prediction.
- Evaluate model performance using classification metrics.
- Save the trained model for future predictions.

---

##  Dataset Preview

Below is a snapshot of the fraud detection dataset used in this project:

![Dataset Preview](images/dataset.png)

---

# 📊 Visualizations

## Transaction Types
![Transaction Types](images/Transactions_Types.png)

## Fraud Rate By Type
![Fraud Rate By Type](images/Fraud_Rate_By_Type.png)

## Transaction Amount Distribution (Log Scale)
![Transaction Amount Distribution](images/Transaction_Amount_Distribution(Log_Scale).png)

## Amount VS isFraud (Filtered Under 50K)
![Amount vs Fraud](images/Amount_VS_isFraud(Filtered_Under_50K).png)

## Frauds Over Time
![Frauds Over Time](images/Frauds_Over_Time.png)

## Fraud Distribution In Transfer And Cash Out
![Fraud Distribution](images/Fraud_Distribution_In_Transfer_And_Cash_Out.png)

## Correlation Matrix
![Correlation Matrix](images/Correlation_Matrix.png)

## Data Information
![Data Info](images/data_info.png)

## Confusion Matrix

![Confusion Matrix](Confusion_Matrix.png)

## Decision Tree Learning Curve

![Learning Curve](Decision_Tree_Learning_Curve.png)

##  Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

---

##  Exploratory Data Analysis (EDA)
The following analysis was performed:

### Transaction Analysis
- Distribution of transaction types
- Fraud rate by transaction type
- Transaction amount distribution
- Fraud trends over time
- Fraud distribution in TRANSFER and CASH_OUT transactions

### Visualizations
- Bar Charts
- Histograms
- Boxplots
- Countplots
- Correlation Heatmap
- Fraud trend line plots

### Key Insights
- Fraud mainly occurs in **TRANSFER** and **CASH_OUT** transactions.
- Certain abnormal balance changes indicate suspicious behavior.
- Fraud cases are highly imbalanced compared to non-fraud cases.

---

## ⚙ Feature Engineering
Created new features to improve model performance:

### 1 Balance Difference Origin
```python
balanceDiffOrig = oldbalanceOrg - newbalanceOrig
```

### 2 Balance Difference Destination
```python
balanceDiffDest = newbalanceDest - oldbalanceDest
```

### 3 Suspicious Zero Balance Transactions
Transactions where balance drops to zero after transfer were analyzed as potential fraud indicators.

---

##  Machine Learning Model
### Algorithm Used
- Logistic Regression

### Preprocessing
- Standard Scaling for numeric features
- One-Hot Encoding for categorical variable
- Train-Test Split
- Pipeline implementation

### Handling Imbalanced Data
Used:
```python
class_weight='balanced'
```

---

##  Model Evaluation
Performance evaluated using:

- Classification Report
- Confusion Matrix
- Accuracy Score

Metrics considered:
- Precision
- Recall
- F1 Score
- Accuracy

---

##  Model Pipeline
Pipeline includes:

1. Data preprocessing  
2. Feature scaling  
3. Encoding categorical data  
4. Logistic Regression classifier  

```python
Pipeline = Pipeline([
 ("prep", preprocessor),
 ("clf", LogisticRegression(class_weight="balanced"))
])
```

---

##  Model Saving
Trained model saved using:

```python
joblib.dump(Pipeline,"fraud_detection_pipeline.pkl")
```

Saved model can be loaded later for predictions.

---

## ▶ How to Run Project

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Run Notebook
```bash
jupyter notebook
```

Open the notebook and run all cells.

---

##  Project Workflow
1. Import Libraries  
2. Load Dataset  
3. Data Cleaning  
4. Exploratory Data Analysis  
5. Feature Engineering  
6. Model Building  
7. Evaluation  
8. Save Model

---

##  Future Improvements
- Random Forest and XGBoost implementation
- Hyperparameter tuning
- Deep learning models
- Real-time fraud detection system
- Deployment using Flask/Streamlit

##  Conclusion
The project demonstrates how machine learning can detect fraudulent financial transactions by analyzing behavioral and transactional patterns. Logistic Regression provided a strong baseline model and can be extended with advanced algorithms for improved performance.

---

##  Author
Shifa Ansari  
Fraud Detection Prediction Model using Machine Learning
