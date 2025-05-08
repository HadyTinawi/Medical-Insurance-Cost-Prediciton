Medical Insurance Cost Prediction
Project Overview
This project demonstrates the application of regression techniques to predict medical insurance costs based on patient attributes such as age, BMI, smoking status, and region. By developing a robust predictive model, we can help individuals and insurance providers estimate healthcare expenses more accurately and identify key cost drivers.
Dataset
The dataset contains information on health insurance beneficiaries including:

Age: Age of the primary beneficiary
Sex: Gender of the insurance contractor (male/female)
BMI: Body Mass Index
Children: Number of dependents covered
Smoker: Smoking status (yes/no)
Region: Residential area in the US (northeast, southeast, southwest, northwest)
Charges: Individual medical costs billed by health insurance (target variable)

Methodology
Data Preprocessing and Feature Engineering

Conducted comprehensive exploratory data analysis
Applied standardization to numerical features
Implemented one-hot encoding for categorical variables
Created domain-specific interaction terms:

Smoker × BMI interaction
Smoker × Age interaction
Squared terms for nonlinear relationships



Model Development
Investigated multiple regression approaches:

Linear Regression (baseline)
Ridge Regression (L2 regularization)
Lasso Regression (L1 regularization)
Polynomial Regression

Implemented robust cross-validation techniques to ensure reliable model evaluation and hyperparameter tuning.
Key Findings
Feature Importance
Our analysis revealed that smoking status is by far the most significant predictor of insurance costs, followed by the interaction between smoking and BMI, age, and other factors.
Model Performance
Ridge Regression provided the best performance with careful hyperparameter tuning, achieving an RMSE of approximately 5378 on validation data and an R² score of 0.82.
Residual Analysis
Residual analysis showed some heteroscedasticity, with model predictions being less accurate for very high insurance costs, particularly among smokers.
Repository Structure
medical-insurance-prediction/
│
├── DC1.ipynb                  # Main Jupyter notebook with analysis and modeling
├── insurance_predictions.csv  # Predictions on the test dataset
├── README.md                  # Project documentation
│
├── data/
│   ├── train_data.csv         # Training features
│   ├── train_labels.csv       # Training target values
│   └── test_data.csv          # Test features
Conclusions
This project successfully demonstrates:

The critical impact of smoking status on insurance costs
The importance of feature engineering in regression problems
The effectiveness of regularization techniques for improved model generalization
How to properly validate and diagnose regression models

The final model provides accurate predictions of medical insurance costs, with reasonable error margins and good explanatory power.
Technologies Used

Python: Main programming language
Pandas & NumPy: Data manipulation
Scikit-learn: Machine learning models and evaluation
Matplotlib & Seaborn: Data visualization
Google Colab: Development environment

Future Work

Explore additional feature transformations for improved model performance
Implement more advanced regression techniques such as Gradient Boosting
Develop an interactive dashboard for insurance cost prediction
Investigate regional variations in more detail
