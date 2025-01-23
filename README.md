# README: Predicting Wine Quality with Machine Learning

## Project Overview
This project focuses on building and improving a machine learning model to predict wine quality based on physicochemical attributes. Through iterative steps including feature engineering, data balancing, and hyperparameter tuning, the model's performance was significantly enhanced.

## Dataset
- **Source**: [Kaggle: White Wine Quality Dataset](https://www.kaggle.com/datasets/piyushagni5/white-wine-quality)
- **Description**: Contains physicochemical properties of white wines and their quality scores (3 to 9).
- **Features**: 11 physicochemical properties such as alcohol, pH, and residual sugar.
- **Target Variable**: Wine quality (integer scores).

## Steps and Methodology

### 1. Baseline Model Performance
- **Objective**: Establish a benchmark for comparison.
- **Results**: 
  - R² Score: 0.546  
  - RMSE: 0.593
- **Insights**: The model struggled with imbalanced data and unexplored feature relationships.

### 2. Feature Engineering
- **Objective**: Enhance the dataset with new meaningful features to improve predictive accuracy.
- **New Features Added**:
  - `sugar_alcohol_ratio`
  - `volatile_acidity_pH_ratio`
  - Interaction terms and other domain-specific features.
- **Impact**: Improved the model's ability to capture complex relationships.

### 3. Addressing Class Imbalance with SMOTE
- **Objective**: Balance the dataset to prevent bias toward majority classes.
- **Method**: Applied Synthetic Minority Oversampling Technique (SMOTE).
- **Result**: The resampled dataset ensured equal representation of all quality levels.

### 4. Hyperparameter Tuning with GridSearchCV
- **Objective**: Optimize XGBoost model parameters for better performance.
- **Key Parameters Tuned**: `n_estimators`, `max_depth`, `learning_rate`, `subsample`.
- **Outcome**:
  - R² Score: 0.954  
  - RMSE: 0.424

### 5. Visualizations and Interpretability
- **Feature Importance**: Identified key features using SHAP and XGBoost.
- **Error Analysis**: Highlighted areas for improvement, particularly for underrepresented quality levels.

## Results Summary
| Metric              | Baseline Model | Improved Model |
|---------------------|----------------|----------------|
| **R² Score**       | 0.546          | 0.954          |
| **RMSE**           | 0.593          | 0.424          |

## Tools and Libraries Used
- **Python Libraries**: pandas, numpy, matplotlib, seaborn, xgboost, scikit-learn, imbalanced-learn, SHAP.

## How to Reproduce
1. Clone the repository and download the dataset.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook to execute the analysis and model training steps.

## Recommendations for Future Work
1. **Feature Engineering**: Explore external data sources or new feature combinations.
2. **Advanced Models**: Experiment with ensemble methods or neural networks.
3. **Explainability**: Utilize advanced interpretability tools like SHAP or LIME.
4. **Validation**: Test the model on an independent validation dataset.

## Conclusion
This project demonstrates how iterative improvements in data preprocessing, feature engineering, and model optimization can lead to significant gains in predictive performance. The resulting model is robust and provides valuable insights into the factors influencing wine quality.

---

### Contact
For questions or collaborations, feel free to reach out at [your_email@example.com].
