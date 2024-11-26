# Titanic Survival Prediction

**Description:**  
A machine learning project focused on predicting the survival of passengers aboard the Titanic based on their characteristics, such as age, gender, class, and more. The analysis utilizes two predictive models: **Logistic Regression** and **K-Nearest Neighbors (KNN)**, providing insights into the factors influencing survival.

---

## 🎯 Objectives

- **Understand survival factors**: Analyze key passenger attributes that influenced survival during the Titanic disaster.
- **Build predictive models**: Create two models, Logistic Regression and KNN, to predict passenger survival.
- **Compare model performance**: Evaluate the effectiveness of both models using metrics like accuracy and confusion matrices.
- **Data visualization**: Generate clear visualizations to illustrate survival trends and model results.

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

## 📊 Results

### Logistic Regression
- **Accuracy**: 81%
- **Precision**: 78%
- **Recall**: 72%
- **F1-Score**: 75%

### K-Nearest Neighbors (KNN)
- **Accuracy**: 79%
- **Precision**: 76%
- **Recall**: 70%
- **F1-Score**: 73%
- **Optimal K**: 5

### Key Insights
- **Gender**: Females had a significantly higher survival rate than males.
- **Passenger Class**: Passengers in first class were more likely to survive compared to those in second and third class.
- **Family Size**: Moderate family sizes (e.g., 1-2 relatives aboard) were associated with higher survival rates.

---

## 📈 Visualizations

Include a few examples of visualizations that help to understand the dataset and results, such as:
1. Survival rates by gender and class.
2. Distribution of ages for survivors vs. non-survivors.
3. Confusion matrices for both models.

Example placeholder for a visualization:

![Survival by Gender](path/to/survival_by_gender.png)

---

## 🗂️ Data Source

The dataset used in this project is the famous **Titanic dataset**, available on [Kaggle](https://www.kaggle.com/c/titanic).

---

## 💻 Installation & Usage

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your_username/titanic-survival-prediction.git
