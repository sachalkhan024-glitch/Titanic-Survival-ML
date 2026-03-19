# Titanic Survival Prediction: Feature Engineering & Random Forest Optimization

### Project Overview
This repository contains a machine learning pipeline to predict passenger survival for the Titanic dataset. The project focuses on improving predictive power through data cleaning, feature engineering, and model optimization.

### Key Results
* **Verified Kaggle Score:** 0.77033
* **Local Validation Accuracy:** 83.24%
* **Model Used:** Random Forest Classifier (100 estimators)

### Technical Workflow

#### 1. Data Cleaning and Preprocessing
* **Handled Missing Data:** Used median imputation for "Age" and "Fare" columns to prevent data loss.
* **Categorical Encoding:** Applied One-Hot Encoding to "Sex" and "Embarked" to convert text into numerical format.
* **Noise Reduction:** Dropped high-cardinality features like "Ticket," "Cabin," and "Name" to prevent overfitting.

#### 2. Feature Engineering
Created a custom **FamilySize** feature by combining "SibSp" (siblings/spouses) and "Parch" (parents/children). 
* **Insight:** This feature captured the survival advantage of small family units compared to solo travelers or very large groups.

#### 3. Model Optimization
The model was built using a **Random Forest Classifier** to capture complex, non-linear patterns in the passenger data.
* **Optimization:** Tested various depth and estimator settings to reach a stable 83.24% accuracy plateau.
* **Reproducibility:** Used a fixed random seed (42) to ensure consistent results.

### Repository Structure
* **titanic_analysis.ipynb:** The complete Python notebook with data cleaning and model training.
* **submission.csv:** The final prediction file uploaded to the Kaggle leaderboard.
