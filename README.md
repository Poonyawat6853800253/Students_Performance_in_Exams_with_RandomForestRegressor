# Students_Performance_in_Exams_with_RandomForestRegressor
This project analyzes the Students Performance in Exams dataset and builds a Random Forest regression model to predict average student scores from demographic and background features. It includes EDA, feature encoding, model evaluation, and feature importance analysis. Created for learning end-to-end regression on tabular data.

# Students Performance in Exams

This project analyzes the **Students Performance in Exams** dataset and builds a **Random Forest Regressor** to predict a student’s average score based on background and demographic features. The notebook covers the full workflow from exploratory data analysis (EDA) to preprocessing, training, evaluation, and interpretation.

## Purpose
This notebook was created to study how machine learning can be used to predict student academic performance from non-score features such as gender, race/ethnicity, parental education, lunch type, and test preparation course.

The goal is to:
- understand patterns in student performance
- build a regression model for average score prediction
- evaluate prediction quality with standard regression metrics
- interpret which features matter most

## What the project does
- Loads and explores the student performance dataset
- Creates a new target variable called **average_score**
- Performs EDA on exam scores and student background features
- Visualizes score distributions and group comparisons
- Encodes categorical variables with one-hot encoding
- Splits the data into training and test sets
- Trains a **Random Forest Regressor**
- Evaluates performance using MAE, MSE, RMSE, and R²
- Compares actual vs predicted values
- Analyzes feature importance
- Includes an edited version with feature engineering for performance improvement

## Dataset Features
The model uses student background information such as:
- **gender**
- **race/ethnicity**
- **parental level of education**
- **lunch**
- **test preparation course**

Target:
- **average_score**

The target is computed as:

average_score = (math score + reading score + writing score) / 3

## Exploratory Data Analysis
The notebook includes:
- score distribution histograms
- boxplots of math, reading, and writing scores
- gender count plots
- average score comparison by test preparation course
- average score comparison by lunch type
- average score comparison by parental education
- correlation heatmap
- scatter plot of reading vs writing score

These analyses help reveal how student background factors relate to academic performance.

## Model Used
### Random Forest Regressor
A tree-based ensemble regression model is used because it:
- works well on tabular data
- can capture non-linear relationships
- is robust to noise
- provides feature importance for interpretation

## Evaluation Metrics
The notebook evaluates the regression model using:
- **MAE** — Mean Absolute Error
- **MSE** — Mean Squared Error
- **RMSE** — Root Mean Squared Error
- **R² Score** — proportion of variance explained by the model

It also visualizes:
- actual vs predicted values
- error tables
- largest prediction errors
- feature importance ranking

## Feature Engineering Version
The notebook also includes an improved version with extra engineered features such as:
- **parent_edu_rank**
- **prep_completed**
- **standard_lunch**
- interaction terms like:
  - **prep_x_lunch**
  - **prep_x_parentedu**

This version is designed to improve performance and make the model more informative.

## Why this project is useful
This project is useful for:
- learning regression on tabular datasets
- practicing full ML workflow from EDA to evaluation
- understanding how categorical features are encoded
- exploring the impact of socioeconomic and educational factors
- building a beginner-friendly education analytics project

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Outputs
The notebook generates:
- summary statistics
- EDA plots
- encoded feature tables
- trained regression model
- regression metrics
- actual vs predicted comparison
- feature importance plots

## Key Learning Outcome
This project shows how student background variables can be used to estimate academic performance, and how machine learning can help identify patterns that may support educational analysis and intervention planning.

## Future Improvements
Possible extensions include:
- comparing Random Forest with Linear Regression, XGBoost, or CatBoost
- performing hyperparameter tuning
- using cross-validation
- testing classification tasks such as pass/fail prediction
- adding fairness analysis across demographic groups
