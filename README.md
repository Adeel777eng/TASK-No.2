# TASK-No.2
# Customer Churn Prediction Pipeline

## 🎯 Objective
Build a production-ready **machine learning pipeline** to predict customer churn using the Telco Churn dataset.  
This project demonstrates the complete ML lifecycle: preprocessing, model training, hyperparameter tuning, evaluation, and model export for reuse.

---

## 📊 Dataset
- **Source:** [Telco Customer Churn Dataset – Kaggle](https://www.kaggle.com/blastchar/telco-customer-churn)  
- **File Required:** `WA_Fn-UseC_-Telco-Customer-Churn.csv` (place in project root directory)  

**Structure:**
- `customerID`: Unique ID for each customer (dropped during preprocessing)  
- `gender`, `Partner`, `Dependents`, etc.: Customer demographics  
- `tenure`, `MonthlyCharges`, `TotalCharges`: Usage and billing details  
- `Churn`: Target variable (`Yes` = 1, `No` = 0)

---

## 🤖 Models Applied
Two classification models were trained and compared:

1. **Logistic Regression**  
   - A baseline linear model for churn classification.  

2. **Random Forest Classifier**  
   - An ensemble model using multiple decision trees to improve prediction accuracy.  

---

## ⚙️ Steps Performed

### 1. Data Preprocessing
- Dropped `customerID` column  
- Converted `TotalCharges` to numeric, handled missing values  
- Applied **Standard Scaling** for numeric features  
- Applied **One-Hot Encoding** for categorical features  

### 2. Train-Test Split
- 80% for training, 20% for testing  
- Stratified split to maintain class balance  

### 3. Model Training
- Built pipelines combining preprocessing + model  
- Trained both Logistic Regression and Random Forest  

### 4. Hyperparameter Tuning
- Used **GridSearchCV** (5-fold cross-validation)  
- Tuned hyperparameters like `C`, `solver` for Logistic Regression and `n_estimators`, `max_depth` for Random Forest  

### 5. Model Evaluation
Metrics used:
- **Accuracy**  
- **Classification Report** (Precision, Recall, F1-score)  

---

## 📈 Key Results (Example)
| Model                | Validation Accuracy (CV) | Test Accuracy |
|-----------------------|--------------------------|---------------|
| Logistic Regression   | 0.80                     | 0.79          |
| Random Forest         | 0.83                     | 0.82          |

---

## 🛠️ Skills Demonstrated
- End-to-End ML pipeline construction with **scikit-learn**  
- **Hyperparameter tuning** with GridSearchCV  
- **Feature engineering** (scaling & encoding)  
- **Pipeline export** using Joblib for production readiness  

---

## 🚀 Future Improvements
- Add advanced models (e.g., XGBoost, LightGBM)  
- Use **SMOTE** or class weights to handle class imbalance  
- Deploy as a web service using **Flask/FastAPI**  
- Add monitoring for data drift in production  

---

## 📂 File Structure
