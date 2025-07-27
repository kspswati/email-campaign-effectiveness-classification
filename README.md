# 📧 Email Campaign Effectiveness Classification

This project applies machine learning to predict how customers interact with email campaigns — whether they ignore, read, or acknowledge the message. It enables marketing teams to better understand campaign performance and optimize communication strategies to improve customer engagement and ROI.

---

## Problem Statement

Email marketing is one of the most widely used methods for customer engagement, yet many campaigns yield low response rates. This project addresses the problem of predicting user behavior in response to an email, using attributes like email content, timing, and historical engagement. By classifying engagement outcomes, businesses can make strategic decisions to improve marketing performance.

---

## Dataset

- **Source**: Provided email campaign dataset  
- **Size**: 68,353 observations × 12 features  
- **Target Variable**: `Email_Status` (Ignored, Read, Acknowledged)  
- **Columns Include**:
  - Email Metadata: `Email_Type`, `Campaign_Type`, `Email_Source`
  - Content Features: `Subject_Hotness_Score`, `Word_Count`, `Total_Links`, `Total_Images`
  - Engagement History: `Total_Past_Communications`
  - Demographics: `Customer_Location`, `Time_Email_Sent`

---

## ⚙️ Algorithms and Models Used

### Data Preprocessing
- Null value imputation (mean for normal, mode for skewed distributions)
- Outlier handling
- Multicollinearity removal using VIF (Variance Inflation Factor)

### Exploratory Data Analysis
- Distribution plots (Seaborn)
- Feature correlation analysis
- Response pattern exploration

### Modeling and Evaluation
- **Baseline Models**:
  - Logistic Regression
  - Decision Tree Classifier
  - K-Nearest Neighbors (KNN)
  - Support Vector Machine (SVM)
- **Advanced Models**:
  - Random Forest Classifier
  - XGBoost Classifier
- **Hyperparameter Tuning**:
  - GridSearchCV for parameters like `max_depth`, `learning_rate`, `n_estimators`
- **Validation**:
  - K-Fold Cross Validation (stratified)

---

## Project Structure

```
📦 Email-Campaign-Effectiveness
├── dataset.csv                 # Campaign engagement data (not shared publicly)
├── proposol.ipynb             # Full notebook: EDA, modeling, evaluation
├── README.md                  # Project documentation
```

---

## 📊 Evaluation Metric

- Accuracy Score (Train/Test split)
- Future scope includes adding:
  - F1-Score
  - ROC-AUC Curve
  - Confusion Matrix

---

## Key Insights

- Engagement is highly influenced by:
  - `Subject_Hotness_Score`  
  - Number of past communications  
  - Email timing (`Time_Email_Sent`)  
- Emails with fewer links and images perform better
- XGBoost and Random Forest consistently outperformed linear models in classification accuracy

---

## Business Value

- **Increased ROI**: Enables more targeted, effective email strategies based on predictive engagement
- **Marketing Efficiency**: Reduces waste on ineffective campaigns and improves conversion rates
- **Scalable Insights**: The same framework can be applied to other outreach channels (e.g., SMS, app notifications)


