# FraudDetectionProject
 Fraud Detection Project
 
🎯 Objective

The goal of this project is to build a machine learning model that identifies fraudulent transactions.
Since the dataset is highly imbalanced (very few fraud cases compared to legitimate ones), special techniques were required to handle the imbalance and evaluate the model properly.

📊 Workflow Overview

1. Data Loading & Preprocessing
2. EDA
3. Data Cleansing: outliers and missing values
4. Feature Engineering
5. Feature selection: Lasso, Ridge
6. Handling Imbalanced Data
  Several resampling techniques were tested:
      * No Balancing (baseline)
      * Random Over Sampling
      * SMOTE
      * SMOTE + Tomek Links
      * Random Under Sampling
  Random Over Sampling demonstrated the best balance between capturing fraud cases and maintaining stable model performance.
7. Model Training & Evaluation
   The following models were evaluated:
      * Decision Tree
      * Random Forest
      * AdaBoost
      * GradientBoosting
      * XGBoost (selected as the best-performing model)
      * SVC
 8. Hyperparameter Tuning (Fine-Tuning)
    Used GridSearchCV to optimize XGBoost parameters

✅ Final Results (After Fine-Tuning)

The model detects 91% of fraud cases (high Recall)
This comes with some false alarms of 3% (lower Precision)
In fraud detection, high Recall is usually more important, because missing fraudulent behavior (False Negative) is more costly than investigating a false alert (False Positive).


🧠 Key Insights & Conclusions

Resampling methods significantly impact fraud detection performance.
Random Over Sampling provided the most practical improvement in detecting fraud cases.
XGBoost outperformed other models due to its ability to capture non-linear patterns.
Fine-Tuning improved Recall substantially, which aligns with business goals for fraud detection.


🧰 Tools & Technologies

Python,
Pandas, 
NumPy,
Scikit-learn,
Matplotlib / Seaborn

📂 Running the Project

These notebooks cannot be executed on Google Colab due to environment and file path dependencies.
They must be run locally on your computer.
Please make sure to download all required files (datasets, notebooks, and scripts) and keep them in the same working directory before running the notebooks.
If needed, install dependencies using: pip install -r requirements.txt

For a detailed summary of the fraud detection project, see the PDF report here: (docs/Credit Card Fraud Detection Project.pdf)

