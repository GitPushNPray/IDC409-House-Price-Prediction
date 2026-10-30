# IDC409 — House Price Prediction

A data science and machine learning project that explores house-price prediction using Python, data cleaning, exploratory data analysis (EDA), feature engineering, SQLite databases, and regression models.

## Project Overview

The objective of this project is to predict house prices using property characteristics such as location, area, number of bedrooms, property type, furnishing status, and other available amenities.

The project demonstrates the complete machine learning workflow, from data preprocessing and database operations to model training, evaluation, and price prediction for a new property.

## Objectives

- Store and manipulate data using **NumPy** and **Pandas**.
- Conduct exploratory data analysis to understand price distributions, location effects, feature relationships, and outliers.
- Understand the available features and investigate feature reduction.
- Train and compare multiple machine learning regression models.
- Evaluate model performance using appropriate metrics.
- Implement a prediction function for a new house.
- Share the project code through GitHub.

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook
- Joblib

## Project Workflow

### 1. Data Cleaning and Preprocessing

The notebook investigates data quality and prepares the dataset for analysis and modelling.

Tasks include:

- Checking for missing values and duplicate records.
- Identifying invalid or inconsistent property values.
- Handling outliers.
- Correcting data inconsistencies where appropriate.
- Removing features that could cause data leakage.
- Preparing categorical and numerical features for modelling.

### 2. Database Operations

SQLite is used to demonstrate database functionality, including:

- Reading records from a database.
- Writing data to database tables.
- Updating existing records.
- Deleting records.
- Storing and retrieving cleaned data.

### 3. Exploratory Data Analysis

EDA is used to investigate the dataset and understand the factors associated with house prices.

The analysis includes:

- Distribution of house prices.
- Price differences across cities.
- Relationship between property size and price.
- Price per square foot.
- Correlation analysis.
- Categorical feature analysis.
- Outlier investigation.
- Residual and prediction-error analysis.

### 4. Feature Engineering and Feature Reduction

Property features are prepared for machine learning. Categorical variables are encoded, and engineered features are created where applicable.

Feature reduction is investigated by comparing a larger feature set with a smaller set of selected features. Potential redundancy and data leakage are also considered.

### 5. Machine Learning Models

The notebook evaluates baseline predictors and several regression algorithms.

| Model | Purpose |
|---|---|
| Mean baseline | Reference prediction using the mean target value |
| Median baseline | Reference prediction using the median target value |
| Linear Regression | Establishes a linear regression baseline |
| Ridge Regression | Applies L2 regularisation |
| Lasso Regression | Applies L1 regularisation |
| Decision Tree Regressor | Learns nonlinear relationships using decision rules |
| Random Forest Regressor | Combines multiple decision trees |
| Gradient Boosting Regressor | Builds an ensemble of sequentially improved trees |

The models are compared to determine whether machine learning provides an improvement over simple baseline predictions.

### 6. Model Evaluation

The following metrics are used to evaluate regression performance:

- **MAE — Mean Absolute Error:** Average absolute prediction error.
- **RMSE — Root Mean Squared Error:** Penalises larger prediction errors more heavily.
- **R² Score:** Measures predictive performance relative to a mean-target baseline.
- **MAPE — Mean Absolute Percentage Error:** Measures average absolute percentage error, with limitations when target values are near zero.

Additional analysis examines residuals, prediction bias across price ranges, and differences between global and city-specific models.

### 7. House Price Prediction

A prediction function accepts details about a new property, prepares its features using the project's preprocessing workflow, and generates an estimated house price.

The output includes an estimated price in Indian rupees and lakhs, along with an approximate residual-based prediction range where available.

**Important:** Predictions depend on the quality and representativeness of the training dataset. The notebook's current evaluation indicates weak predictive performance, so its price estimates should not be treated as reliable real-estate valuations.

### 8. Price Category Classification

The project also explores an extension that classifies properties into price categories such as Low, Medium, and High, and evaluates the classification results using appropriate metrics.

## Repository Contents

- `IDC409_DS___AI__Project_House_Price_Prediction_1.ipynb` — Main Jupyter Notebook containing the analysis, database operations, model training, evaluation, and prediction workflow.

Additional datasets, trained models, or output files may be added as the project develops.

## How to Run

### Prerequisites

Install Python and Jupyter Notebook, then install the required libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn joblib jupyter
```

SQLite support is included with standard Python installations.

### Steps

1. Clone or download this repository.
2. Open a terminal in the project directory.
3. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Open `IDC409_DS___AI__Project_House_Price_Prediction_1.ipynb`.
5. Ensure the required dataset and any referenced model or output files are available in their expected paths.
6. Run the notebook cells in order.

Some cells may require adjustment if the dataset or generated model files are not included in the repository.

## Limitations and Future Improvements

The current analysis indicates that the dataset has weak relationships between house prices and the available property features. Consequently, the trained models do not yet demonstrate reliable individual price predictions.

Potential improvements include:

- Using a more representative real-estate dataset.
- Improving missing-value and outlier handling.
- Investigating feature relevance and data leakage.
- Using cross-validation and systematic hyperparameter tuning.
- Comparing performance across cities and price ranges.
- Improving prediction reliability and uncertainty estimation.
- Developing a simple interface for entering property details and obtaining predictions.

## Academic Context

**Course:** IDC409 — Data Science and Artificial Intelligence  
**Project:** House Price Prediction  
**Institution:** IISER Mohali

## Disclaimer

This project is intended for academic learning and demonstration of data science and machine learning techniques. Its predictions are experimental and should not be used as the basis for real-estate purchases, sales, or investments.

## License

No license has been specified for this repository.
