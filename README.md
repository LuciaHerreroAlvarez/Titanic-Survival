# Titanic Survival Prediction

## Description:
A machine learning project focused on predicting the survival of passengers aboard the Titanic based on their characteristics, such as age, gender, class, and more. The analysis utilizes two predictive models: Logistic Regression and K-Nearest Neighbors (KNN), providing insights into the factors influencing survival.

---

## 📑 Table of Contents
- [Objectives](#-objectives)
- [Summary](#-summary)
- [Data Source](#-data-source)
- [Methodology](#-methodology)
- [Results](#-results)

---

## 🎯 Objectives
- **Understand survival factors:** Analyze key passenger attributes that influenced survival during the Titanic disaster.
- **Build predictive models:** Create two models, Logistic Regression and KNN, to predict passenger survival.
- **Compare model performance:** Evaluate the effectiveness of both models using metrics like accuracy, confusion matrices, and ROC AUC.
- **Data visualization:** Generate clear visualizations to illustrate survival trends and model results.

---

## 📊 Summary

### Conclusions:

#### Logistic Regression:
- **Accuracy:** 93.06%
- **Sensitivity:** 89.47%
- **Specificity:** 95.11%
- **ROC AUC:** 0.976, indicating excellent model performance.

#### K-Nearest Neighbors (KNN):
- **Accuracy:** 65.31%
- **Sensitivity:** 53.29%
- **Specificity:** 72.18%
- **ROC AUC:** (not calculated, please compute if needed).

### Key Factors Influencing Survival:
- **Gender:** Females had a significantly higher survival rate than males.
- **Class:** Passengers in first class had a much higher likelihood of survival compared to second and third class.
- **Age:** Younger passengers and children showed better survival rates.

### Model Comparison:
- **Logistic Regression** outperformed KNN across all metrics, proving to be a more suitable model for this dataset.

### Notes:
- The **IsMinor** feature added valuable insights into the survival prediction model, potentially influencing how age impacted survival.

---

## 🗂️ Data Source
The dataset used in this project is the famous Titanic dataset, available on Kaggle: https://www.kaggle.com/competitions/titanic

---

## 📝 Methodology

### Data Overview
The dataset used in this project comes from Kaggle's Titanic dataset. It contains information about passengers, including:

- Passenger ID
- Survival (1 = Survived, 0 = Did not survive)
- Passenger class (Pclass)
- Gender
- Age
- SibSp (Number of siblings/spouses aboard)
- Parch (Number of parents/children aboard)
- Ticket
- Fare
- Cabin
- Embarked (Port of embarkation)

### Data Cleaning & Preprocessing

- **Handling missing data:**
  - Filled missing ages using the median value for the 'Age' column.
  - Imputed missing embarked values with the mode.

- **Feature encoding:** Converted categorical variables (e.g., gender, embarked) into numerical values using one-hot encoding.

- **Feature selection:** Selected relevant features like age, gender, class, SibSp, and Parch for modeling.

### Feature Engineering:
- **IsMinor:** Added a column indicating whether a passenger was a minor (age < 16) to explore its impact on survival.

### Models Implemented:
- **Logistic Regression:** A simple and interpretable algorithm for binary classification. Provides insights into the importance of individual features.
- **K-Nearest Neighbors (KNN):** A non-parametric model that classifies passengers based on the similarity to their nearest neighbors.

### Model Evaluation:
- **Train-Test Split:** Data was divided into 80% training and 20% testing sets.
- **Metrics:** Evaluated models using accuracy, precision, recall, and F1-score.
- **Hyperparameter Tuning:** Performed grid search to optimize the number of neighbors for KNN.

---

## 🏆 Results

### Logistic Regression

#### Confusion Matrix:
| Predicted | 0    | 1    |
|-----------|------|------|
| Actual 0  | 253  | 13   |
| Actual 1  | 16   | 136  |

- **Accuracy:** 93.06%
- **Sensitivity:** 89.47%
- **Specificity:** 95.11%
- **ROC AUC:** 0.976

### K-Nearest Neighbors (KNN)

#### Confusion Matrix:
| Predicted | 0    | 1    |
|-----------|------|------|
| Actual 0  | 192  | 74   |
| Actual 1  | 71   | 81   |

- **Accuracy:** 65.31%
- **Sensitivity:** 53.29%
- **Specificity:** 72.18%
- **ROC AUC:** (Not calculated; consider calculating for completeness)
