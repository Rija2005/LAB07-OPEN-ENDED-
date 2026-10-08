# LAB07-OPEN-ENDED-
# Employee Attrition Analyzer

## 1. Dataset Description

For this project, the **IBM HR Analytics Employee Attrition & Performance** dataset was used. The dataset contains information about employees, such as age, job role, monthly income, job satisfaction, overtime, years at the company, and other work-related factors.

The target variable is **Attrition**, which shows whether an employee left the company or not.

* **Yes = 1** → Employee left the company
* **No = 0** → Employee stayed in the company

The dataset was downloaded using KaggleHub and loaded into Python using Pandas.

---

## 2. Data Preprocessing

Before training the machine learning models, the dataset was prepared using the following steps:

1. **Checked the dataset** using `head()`, `shape`, `info()`, and missing-value checking.
2. **Removed unnecessary columns** such as EmployeeCount, EmployeeNumber, Over18, and StandardHours because they were not useful for prediction.
3. **Converted the target variable** Attrition from Yes/No into 1/0.
4. **Converted categorical data into numerical values** using `pd.get_dummies()`.
5. **Separated the features and target variable**.
6. **Split the dataset** into 80% training data and 20% testing data.
7. **Applied StandardScaler** to scale the features for Logistic Regression.

These preprocessing steps made the dataset suitable for machine learning models.

---

## 3. Machine Learning Models Used

Three classification models were used in this project:

### Logistic Regression

Logistic Regression was used as a basic classification model to predict whether an employee is likely to leave or stay.

### Decision Tree

Decision Tree was used to make predictions by creating decision rules based on employee features.

### Random Forest

Random Forest combines multiple decision trees and uses their combined predictions to make the final classification. It was also used to identify the most important features related to employee attrition.

All three models were trained using the training data and tested using the same test data so their performance could be compared fairly.

---

## 4. Model Evaluation

The models were evaluated using:

* **Accuracy Score** – shows the percentage of correct predictions.
* **F1 Score** – combines precision and recall and is useful for evaluating classification performance.
* **Confusion Matrix** – shows correct and incorrect predictions for employees who stayed and employees who left.

Confusion matrices were created for all three models to understand their prediction results in more detail.

A **feature importance graph** was also created using the Random Forest model. It shows which employee-related features had the greatest influence on the model's predictions.

The actual accuracy and F1 scores were obtained after running the models on the test data. The model with the better evaluation results can be considered the better-performing model for this dataset.

