## Medical Insurance Cost Prediction

### Project Overview

This project aims to predict the **premium price of a medical insurance policy** based on an individual's health and lifestyle factors. By analyzing features such as age, presence of chronic diseases, height, weight, and family history of cancer, the goal is to develop a regression model that can accurately estimate insurance costs. This is a crucial task for insurance companies in risk assessment and pricing.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Medical Insurance Premium Prediction](https://www.kaggle.com/datasets/tejashvi14/medical-insurance-premium-prediction)
  * **Size**: 986 entries, 11 columns
  * **Key Features**:
      * `Age`, `Diabetes`, `BloodPressureProblems`, `AnyTransplants`, `AnyChronicDiseases`, `Height`, `Weight`, `KnownAllergies`, `HistoryOfCancerInFamily`, `NumberOfMajorSurgeries`.
  * **Approach**:
      * **Data Cleaning**: The dataset was clean with no missing values or duplicates.
      * **Exploratory Data Analysis**: Histograms, boxplots, and scatter plots were used for visualization to understand data distributions and the relationship between features and the target variable `PremiumPrice`. A correlation heatmap was also generated.
      * **Data Standardization**: The `Age` column was standardized using `StandardScaler`, and the rest of the features were also scaled before model training.
      * **Regression Task**: The target variable is `PremiumPrice`.
      * **Models Used**:
          * A suite of regression models were trained, including Ridge, XGBoost, Random Forest, AdaBoost, Gradient Boosting, Bagging, Decision Tree, SVR, and K-Nearest Neighbors (KNN).
  * **Best R² Score**:
      * **0.860** with Random Forest Regressor.
      * **0.855** with Gradient Boosting Regressor.
      * **0.824** with Bagging Regressor.
      * The high R² scores for the ensemble models indicate that these health metrics are strong predictors of insurance premium prices.

-----

### Purpose and Applications

  * Enable insurance companies to **accurately price medical premiums** based on an individual's risk profile.
  * Assist in risk assessment for new insurance applicants.
  * Support data-driven decision-making in insurance product development.
  * Provide a tool for individuals to understand how their health and lifestyle factors influence their insurance costs.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Medical-Insurance-Cost-Prediction-Using-ML.git
cd Medical-Insurance-Cost-Prediction-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Performing comprehensive hyperparameter tuning and cross-validation for the top-performing regression models.
  * Exploring more advanced feature engineering techniques, such as creating a BMI feature from `Height` and `Weight`.
  * Investigating alternative scaling methods or outlier handling strategies.
  * Adding explainability (e.g., SHAP or LIME) to understand which health factors are the most significant drivers of premium prices.
