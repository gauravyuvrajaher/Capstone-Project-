# Capstone-Project-
Peer-to-Peer Credit Risk Analysis (Lending Club)
🔍 Project Overview

Peer-to-peer (P2P) lending platforms offer higher returns to investors but come with significant credit default risk.
This project analyses historical Lending Club loan data to identify high-risk borrowers, reduce default risk, and support data-driven lending decisions.

The objective is to predict whether a borrower will fully repay or default (charged-off) on a loan, while prioritising business-relevant outcomes such as reducing false negatives (missed defaulters).

🎯 Business Problem

Incorrectly approving a high-risk borrower leads to financial loss for lenders.
The challenge is to:

Identify borrower segments with higher default probability

Build predictive models that minimise false negatives

Translate model outputs into actionable credit risk insights

📊 Dataset

Source: Lending Club (Kaggle)

Records: ~396,000 loans

Features: 27 (after cleaning)

Target Variable: loan_status

0 → Fully Paid

1 → Charged Off (Default)

Redundant columns such as sub_grade, emp_title, and title were removed.

🧹 Data Preparation & EDA

Key steps included:

Handling missing values using business logic (e.g., imputing loan purpose)

Treating extreme values using log, square-root, and Box-Cox transformations

Detecting and addressing multicollinearity using VIF and PCA

Univariate, bivariate, and multivariate analysis to uncover default drivers

Key Insights

Month-to-month and shorter tenure loans show higher default risk

Borrowers with rented homes default more frequently

Default rates increase with number of open credit lines and public records

🧠 Modeling Approach

Multiple models were evaluated with a focus on reducing false negatives:

Logistic Regression (baseline & PCA-based)

Decision Tree (with pruning)

Random Forest

Gradient Boosting

XGBoost (with RFE)

SMOTE-based oversampling for class imbalance

📌 Evaluation metrics prioritised recall and business risk, not just accuracy.

🏆 Best Performing Model

XGBoost with RFE + Oversampling

Reduced false negatives by ~50%

Improved recall from 7% → 56%

Achieved better balance between bias and variance

📈 Business Impact

Enables lenders to proactively identify high-risk borrowers

Supports risk-based pricing and approval strategies

Can significantly reduce default-related financial losses

⚠️ Limitations & Future Work

Further hyperparameter tuning

Cost-sensitive threshold optimisation

Deployment as a real-time risk scoring API

Continuous model retraining with new loan data

🛠 Tech Stack

Python (pandas, numpy, scikit-learn)

XGBoost

Matplotlib / Seaborn

Jupyter Notebook

👤 Author

Gaurav Aher
