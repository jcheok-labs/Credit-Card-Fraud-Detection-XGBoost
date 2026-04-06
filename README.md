# 💳 Credit Card Fraud Detection: XGBoost & Anomaly Detection

This project builds a machine learning model using **XGBoost** to detect fraudulent credit card transactions in a highly imbalanced dataset. It incorporates **anomaly detection concepts**, **SMOTE resampling**, **threshold tuning**, and **feature importance analysis** to improve identification of rare fraud cases while maintaining overall model performance.

---

## 🚀 Project Overview
- Performed data preprocessing, scaling, and duplicate handling
- Explored class imbalance and transaction characteristics via **visual analysis**
- Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to balance training data
- Conducted **feature importance analysis** using **Mutual Information** and **XGBoost**
- Optimized model hyperparameters with **Optuna**, maximizing **AUPRC**
- Tuned **classification thresholds** to optimize F1-score
- Evaluated model using **precision, recall, F1-score, ROC-AUC**, and **confusion matrices**
- Visualized distributions, correlations, and feature importance plots

---

## 🛠️ Tools & Technologies
- **Python**
- **XGBoost**
- **Scikit-learn** (model evaluation, preprocessing, SMOTE)
- **Imbalanced-learn** (SMOTE)
- **Pandas, NumPy**
- **Matplotlib, Seaborn**
- **Optuna** (hyperparameter optimization)

---

## 📂 Dataset
**Kaggle Dataset:**  
[Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)  

> Note: Dataset exceeds GitHub upload limits (>25MB), so it is hosted externally.

---

## 📊 Exploratory Data Analysis (EDA)
- Class distribution is highly imbalanced (~1:283 ratio)
- Visualized transaction **amount distribution**, **hourly fraud rate**, and **feature correlations**
- Identified top discriminative features correlated with fraud: **V14, V17, V12, V10, V16, V3**

---

## 📈 Key Results
- Optimized XGBoost model achieved:
  - **High recall for fraud detection (~82%)**
  - **Moderate precision (~48%)**, reflecting trade-off with false positives
  - **Near-perfect overall accuracy (~100%)** due to majority class
- **Threshold tuning** improved F1-score for rare fraud cases
- **Feature importance** highlighted key variables contributing to fraud detection, consistent with mutual information scores

---

## 💼 Business Implications
- Enhances fraud detection capabilities, reducing potential financial losses
- High recall ensures most fraudulent transactions are captured
- Can be integrated into **real-time transaction monitoring systems**
- Supports risk management and compliance efforts in financial institutions

---

## ✅ Strengths
- Handles highly imbalanced data effectively using **SMOTE**
- Strong performance in detecting rare fraud cases
- Combines **statistical** (Mutual Information) and **model-based** feature importance
- Scalable and efficient using **XGBoost**
- Threshold tuning allows customization for business priorities (precision vs. recall)

---

## ⚠️ Limitations
- Moderate precision may cause false positives impacting user experience
- Model performance influenced by class imbalance and synthetic sampling
- Feature interpretability limited due to PCA-transformed variables (`V1–V28`)
- Results may vary with different data distributions

---

## 📊 Recommendations
- Fine-tune **classification thresholds** to balance recall vs. false positives
- Explore ensemble or hybrid anomaly detection approaches
- Apply **SHAP** for deeper model explainability
- Continuously retrain with updated transaction data
- Incorporate **cost-sensitive learning** to penalize misclassifications differently

---

## 🔍 Model Explainability
- **Mutual Information:** Identifies individually informative features before modeling
- **XGBoost Feature Importance:** Captures feature contributions within the trained model
- Recommended tool: **SHAP** for detailed, local and global interpretability

---

## 📌 Conclusion
The XGBoost model demonstrates strong capability in detecting fraudulent transactions, especially rare fraud cases in an imbalanced dataset. Threshold tuning and explainability techniques provide further opportunities for improvement, delivering a robust and scalable fraud detection solution.
