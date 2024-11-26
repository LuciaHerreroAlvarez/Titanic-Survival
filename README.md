# Titanic Survival Prediction

**Description:**  
A machine learning project focused on predicting the survival of passengers aboard the Titanic based on their characteristics, such as age, gender, class, and more. The analysis utilizes two predictive models: **Logistic Regression** and **K-Nearest Neighbors (KNN)**, providing insights into the factors influencing survival.

## 📑 Table of Contents

2. [Objectives](#objectives)
3. [Summary](#summary)
4. [Data Source](#data-source)
5. [Methodology](#methodology)
6. [Results](#results)

---

## 🎯 Objectives

- **Understand survival factors**: Analyze key passenger attributes that influenced survival during the Titanic disaster.
- **Build predictive models**: Create two models, Logistic Regression and KNN, to predict passenger survival.
- **Compare model performance**: Evaluate the effectiveness of both models using metrics like accuracy and confusion matrices.
- **Data visualization**: Generate clear visualizations to illustrate survival trends and model results.

---

## 📊 Summary

### Conclusions:

1. **Logistic Regression**:
   - Achieved an **accuracy of 93%**, with strong sensitivity and specificity.
   - The **ROC AUC** score was **0.98**, indicating excellent model performance.

2. **K-Nearest Neighbors (KNN)**:
   - Achieved an **accuracy of 65%** with moderate sensitivity and specificity.
   - The **ROC AUC** score was lower than Logistic Regression, at **0.72**.

3. **Key Factors Influencing Survival**:
   - **Gender**: Females had a significantly higher survival rate than males.
   - **Class**: Passengers in first class had a much higher likelihood of survival compared to second and third class.
   - **Age**: Younger passengers and children showed better survival rates.

4. **Model Comparison**:
   - Logistic Regression outperformed KNN across all metrics, proving to be a more suitable model for this dataset.

---

## 🗂️ Data Source

The dataset used in this project is the famous **Titanic dataset**, available on [Kaggle](https://www.kaggle.com/c/titanic).

---

## 📝 Methodology

### Data Overview
The dataset used in this project comes from **Kaggle's Titanic dataset**. It contains information about passengers, including:
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
1. **Handling missing data**: 
   - Filled missing ages using median values based on passenger class and gender.
   - Imputed missing embarked values with the mode.
2. **Feature encoding**: Converted categorical variables (e.g., gender, embarked) into numerical values.
3. **Normalization**: Scaled continuous features (e.g., age, fare) to improve model performance.
4. **Feature selection**: Selected relevant features like age, gender, class, SibSp, and Parch for modeling.

### Models Implemented
- **Logistic Regression**:
  - A simple and interpretable algorithm for binary classification.
  - Provides insights into the importance of individual features.
- **K-Nearest Neighbors (KNN)**:
  - A non-parametric model that classifies passengers based on the similarity to their nearest neighbors.

### Model Evaluation
- **Train-Test Split**: Data was divided into 80% training and 20% testing sets.
- **Metrics**: Evaluated models using accuracy, precision, recall, and F1-score.
- **Hyperparameter Tuning**: Performed grid search to optimize the number of neighbors for KNN.

---

## 📈 Results

### Logistic Regression
#### Confusion Matrix
| Predicted | 0    | 1    |
|-----------|------|------|
| **Actual 0** | 253  | 13   |
| **Actual 1** | 16   | 136  |

- **Accuracy**: 93.06%
- **Sensitivity**: 89.47%
- **Specificity**: 95.11%
- **ROC AUC**: 0.98

### K-Nearest Neighbors (KNN)
#### Confusion Matrix
| Predicted | 0    | 1    |
|-----------|------|------|
| **Actual 0** | 192  | 74   |
| **Actual 1** | 71   | 81   |

- **Accuracy**: 65.31%
- **Sensitivity**: 53.29%
- **Specificity**: 72.18%
