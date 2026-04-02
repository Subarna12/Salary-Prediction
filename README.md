Income Prediction Using Machine Learning
🚀 Project Overview

This project predicts whether an individual earns more than $50K per year based on demographic and employment data.

It demonstrates a complete ML workflow: from data cleaning, feature engineering, and class balancing, to model training, evaluation, and prediction.

Focus: Applying machine learning theory to real-world data while producing interpretable insights.

📊 Dataset
Source: einkommen_with_headers.csv (Adult Census Income dataset)
Rows: 30,001
Target variable: Income (>50K = 1, <=50K = 0)
Features include:
Age, Education level, Schooling/Training Period
Employment type, Marital status, Gender, Ethnicity
Country of birth, hours-per-week, and more
Mix of categorical and numerical features with some missing values
⚙️ Project Workflow
1️⃣ Data Preprocessing
Remove extra spaces; replace "?" and empty strings with NaN
Fill missing categorical values with the most frequent category
Encode ordinal features (Level of education, Schooling/Training Period)
One-hot encode nominal features (Employment type, Marital status, Gender, etc.)
Convert boolean features to 0/1
Scale numerical features using MinMaxScaler
Balance classes with SMOTE
2️⃣ Modeling

Logistic Regression (Baseline)

Simple linear model for benchmarking
Hyperparameter tuning (C) via GridSearchCV
Classification threshold: 0.4

Random Forest

Captures non-linear feature interactions
Hyperparameter tuning: max_depth and min_samples_split
Performs better for minority class (>50K)
3️⃣ Evaluation
Accuracy, Precision, Recall, F1-score
Confusion Matrix
ROC Curve / AUC
Precision-Recall Curve
🏆 Results

Test data performance:

Model	Accuracy	Precision	Recall	F1-score	ROC-AUC
Logistic Regression	0.83	0.84	0.83	0.83	0.89
Random Forest	0.89	0.89	0.89	0.89	0.95

Insights:

Random Forest outperforms Logistic Regression ✅
Most predictive features: Education level, Employment type, Years of schooling
SMOTE improved predictions for high-income class
📈 Visualizations
Target variable distribution
ROC and Precision-Recall curves
Feature importance plot from Random Forest

All visualizations are included in the notebook and results/ folder.

📂 Predictions
Predictions generated for unlabeled data (rows 5001–30,001)
Saved in predictions_random_forest.csv
💻 How to Run
Clone the repository:
git clone https://github.com/YOUR_USERNAME/income-prediction.git
cd income-prediction
Open the notebook in Google Colab or Jupyter Notebook
Run all cells to reproduce the full ML pipeline
🎯 Conclusion & Next Steps
Demonstrates a full ML workflow from raw data to actionable insights
Future improvements:
Try XGBoost or Gradient Boosting
Additional feature engineering
More extensive hyperparameter tuning and cross-validation
