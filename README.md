# Titanic Survival Analysis and Modeling
This project involves an end-to-end data analysis and predictive modeling pipeline using the Titanic dataset. The objective is to analyze passenger data to predict survival using various machine learning algorithms and handle typical data preprocessing challenges.

### Dataset
The dataset used is the classic Titanic dataset, which includes details about the passengers such as:

PassengerId

Survived

Pclass

Name

Sex

Age

SibSp

Parch

Ticket

Fare

Cabin

Embarked

### Steps Performed
1. Data Loading & Exploration
Loaded the dataset using Pandas.

Performed initial exploration (head(), info(), describe()).

Checked for duplicates and null values.

2. Handling Missing Values
Filled missing Age values using median.

Filled missing Embarked values using mode.

Dropped Cabin column due to over 77% missing data.

3. Data Cleaning & Feature Engineering
Identified categorical and numerical columns.

Created new features like:

FamilySize = SibSp + Parch + 1.

IsAlone = 1 if alone, 0 otherwise.

FareBin and AgeBin for discretization.

Encoded categorical features (Sex, Embarked) using Label Encoding.

4. Outlier Detection & Handling
Used boxplots and IQR method to detect and remove outliers from numeric columns.

5. Correlation Analysis
Created a heatmap of correlations.

Identified key variables like Fare, Pclass, FamilySize influencing survival.

6. Modeling
Split the dataset into training and test sets.

Used Logistic Regression for baseline modeling.

Addressed class imbalance using:

class_weight='balanced'.

SMOTE oversampling.

Built and evaluated a Random Forest Classifier with GridSearchCV and Cross-validation.

Evaluated models using:

Accuracy.

Confusion Matrix.

F1 Score.

ROC-AUC.

### Key Findings
Higher Fare and lower Pclass are associated with higher survival chances.

Feature engineering (like IsAlone, FamilySize) improved the model.

Random Forest with balancing techniques provided the best performance.

### Technologies Used
Python 3.x

Pandas

NumPy

Scikit-Learn

Seaborn

Matplotlib

Imbalanced-learn (SMOTE)

### References
Scikit-Learn RandomForestClassifier

Scikit-Learn GridSearchCV

Titanic Dataset
