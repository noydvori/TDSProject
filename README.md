# **Wine Quality Prediction Project**

## **Overview**
This project focuses on building and improving a predictive model for wine quality using chemical properties as input features. The dataset contains information about white wines, including attributes like acidity, alcohol content, and density. The project is divided into two main parts:

1. **Part 1**: Data exploration, preprocessing, and feature engineering.
2. **Part 2**: Model training, hyperparameter optimization, and performance evaluation.

The goal is to provide actionable insights and build a reliable tool for predicting wine quality while addressing challenges such as class imbalance and model interpretability.

---

## **Table of Contents**
1. [Dataset Description](#dataset-description)
2. [Key Features and Findings](#key-features-and-findings)
3. [Implementation Details](#implementation-details)
4. [Results](#results)
6. [Potential Applications](#potential-applications)

---

## **Dataset Description**
The dataset contains several chemical properties of white wine samples, such as:
- **Fixed Acidity**
- **Volatile Acidity**
- **Citric Acid**
- **Residual Sugar**
- **Density**
- **pH**
- **Alcohol**
- **Wine Quality** (target variable, ranging from 3 to 9)

Key challenges include:
- **Class imbalance**: Some quality levels (e.g., 3 and 9) are underrepresented.
- **Feature correlation**: Understanding interactions between chemical properties is crucial.

---

## **Key Features and Findings**
### Feature Engineering:
- New features created to enhance predictive power:
  - **Volatile Acidity to Citric Acid Ratio**: Measures balance between acidity types.
  - **Density-Alcohol Ratio**: Highlights the relationship between density and alcohol content.
  
### Model Improvements:
- Addressed class imbalance using SMOTE (Synthetic Minority Oversampling Technique).
- Optimized hyperparameters using `GridSearchCV`.

### Insights:
- Relationships between chemical properties significantly impact wine quality.
- The model benefits from engineered features and balanced datasets.

---

## **Implementation Details**
### Part 1: Data Preprocessing and Feature Engineering
- **Exploratory Data Analysis**: Visualized target distribution and feature correlations.
- **Feature Engineering**: Added domain-relevant features to enhance model performance.
- **Data Balancing**: Applied SMOTE to address class imbalance.

### Part 2: Model Training and Evaluation
- **Baseline Model**: Initial evaluation using default hyperparameters.
- **Hyperparameter Optimization**: Conducted grid search for parameters like `n_estimators`, `max_depth`, and `learning_rate`.
- **Evaluation Metrics**: Used R², MSE, and RMSE to measure performance.

---

## **Results**
- **Baseline Model**: Achieved an R² score of ~0.5 with limited generalization.
- **Improved Model**: After applying SMOTE and hyperparameter tuning, the R² score improved to ~0.8, with reduced error metrics.
- **Feature Importance**: The new features contributed significantly to the improved performance.

---

## **Potential Applications**
- **Wine Industry**:
  - Quality prediction for wine producers to maintain standards.
  - Optimizing chemical composition for better-quality wines.
- **Marketing**:
  - Targeted campaigns based on wine quality insights.
- **Predictive Tools**:
  - Develop user-friendly applications for real-time wine quality prediction.

---

## **Contributors**
- **Noy Dvori** - Data Analysis, Feature Engineering, Model Training.
