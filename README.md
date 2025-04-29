# Credit-card-fraud-detection
This project aims to develop a robust classification model to detect fraudulent credit card transactions using real-world data. The primary challenge addressed is **class imbalance**, where fraudulent transactions represent less than 0.2% of all records. This problem is tackled using **SMOTE**, feature engineering, and evaluation strategies focused on minimizing false negatives while maintaining high precision.

---

## 📌 Project Objectives

- Detect fraudulent credit card transactions with high accuracy.
- Handle extreme class imbalance using appropriate sampling techniques.
- Engineer meaningful features that highlight suspicious transaction patterns.
- Evaluate models using precision, recall, F1-score, and ROC-AUC to ensure reliable performance.

---

## 📂 Dataset

- The dataset used is publicly available on Kaggle and contains anonymized credit card transactions from European cardholders (September 2013).
- **Total Records**: 284,807  
- **Fraudulent Transactions**: 492 (≈0.172%)
- **Features**:
  - `Time` and `Amount` are original features.
  - `V1` to `V28` are anonymized via PCA.
  - `Class`: Target variable (1 = fraud, 0 = normal)

---

## 🛠️ Technologies Used

- Python (NumPy, Pandas, Matplotlib, Seaborn)
- Scikit-learn (SMOTE, Logistic Regression, Random Forest, Decision Tree)
- Imbalanced-learn (`imblearn`) for oversampling
- Jupyter Notebook

---

## 🚀 Project Workflow

### 1. Data Loading & Inspection
- Read CSV data
- Basic stats, missing value check, class distribution

### 2. Exploratory Data Analysis (EDA)
- Distribution plots of transaction amount and time
- Fraud vs normal class pattern exploration

### 3. Class Imbalance Handling
- Visualized fraud/normal imbalance
- Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to generate synthetic minority samples

### 4. Feature Engineering
- Used PCA-transformed features (`V1`–`V28`)
- Included `Amount` and `Time` for modeling

### 5. Model Training
- Trained and compared **Logistic Regression**, **Decision Tree**, and **Random Forest**
- Focus on recall and F1-score to ensure fraudulent transactions are captured

### 6. Evaluation Metrics
- Confusion Matrix
- Precision, Recall, F1-Score
- ROC Curve and AUC score

---

## 🧾 Results & Conclusion

- **Random Forest** performed best with high recall and acceptable false positive rate.
- **SMOTE** significantly improved the model's ability to detect fraud.
- Balanced metrics ensured minimal disruption for genuine users while maximizing fraud capture.

---

## 🔮 Future Enhancements

- Deploy real-time fraud detection using stream data tools (e.g., Kafka + Spark).
- Experiment with ensemble learning (e.g., XGBoost, LightGBM).
- Introduce cost-sensitive learning or anomaly detection techniques.
- Visualize and interpret PCA components for explainability.

---

## 📜 License

This project is for educational purposes and follows open data license terms.
