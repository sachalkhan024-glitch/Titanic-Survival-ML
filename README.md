# Titanic-Survival-ML
# Titanic Survival Prediction: Feature Engineering & Random Forest Optimization

![Kaggle Score](https://img.shields.io/badge/Kaggle-0.77033-blue) 
![Python](https://img.shields.io/badge/Python-3.8+-green)

## 📌 Project Overview
This project involves building a predictive model to determine passenger survival during the Titanic shipwreck. The goal was to move beyond basic classification and achieve higher accuracy through **Feature Engineering** and **Hyperparameter Tuning**.

## 🚀 Key Achievements
* **Final Accuracy:** Achieved **83.24%** local validation accuracy.
* **Kaggle Global Rank:** Verified public score of **0.77033**.
* **Feature Innovation:** Created a custom `FamilySize` feature which improved model performance by identifying survival patterns in household groups.

## 🧠 Technical Workflow

### 1. Data Preprocessing & Cleaning
* Handled missing values in `Age` and `Fare` using **Median Imputation** to maintain data distribution.
* Converted categorical variables (`Sex`, `Embarked`) into numerical format using **One-Hot Encoding**.
* Dropped low-variance features like `PassengerId`, `Name`, and `Ticket` to reduce model noise.

### 2. Feature Engineering
* **FamilySize:** Combined `SibSp` (siblings/spouses) and `Parch` (parents/children) into a single metric. 
* *Insight:* Data showed that passengers traveling in small families had a higher survival rate than those traveling alone or in very large groups.

### 3. Model Selection: Random Forest
I chose the **Random Forest Classifier** over Logistic Regression to better handle non-linear relationships. 
* **Optimization:** Tested various `n_estimators` and `max_depth` settings to find the "sweet spot" before overfitting.
* **Final Parameters:** `n_estimators=100`, `random_state=42`.

## 📂 How to Run
1. Clone the repo: `git clone https://github.com/YOUR_USERNAME/Titanic-Survival-ML.git`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the Jupyter Notebook: `jupyter notebook titanic_analysis.ipynb`

## 📈 Future Improvements
* Implement **XGBoost** or **LightGBM** for potentially higher accuracy.
* Extract titles (Mr., Mrs., Master.) from the `Name` column for more granular feature engineering.

