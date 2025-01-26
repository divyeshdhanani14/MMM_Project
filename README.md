# Market Mix Modelling (MMM) for Sales Prediction

This project explores how various marketing channels contribute to overall sales using Market Mix Modelling (MMM). The goal is to analyze the relationship between marketing spend (TV, digital, radio) and sales, and evaluate model performance using Linear and Ridge regression models.

## Objective

The primary objective is to build a predictive model that can estimate the impact of different marketing channels on sales. This can help businesses allocate resources efficiently across various marketing efforts.

## Data

- **Synthetic Data**: Data is synthetically generated with marketing spend on TV, digital, and radio channels along with sales data. Seasonal effects and noise are added to simulate real-world market conditions.
- **Columns**:
  - `time`: Time period (months)
  - `tv_spend`: TV marketing spend
  - `digital_spend`: Digital marketing spend
  - `radio_spend`: Radio marketing spend
  - `sales`: Sales data (target variable)

## Steps in the Project

1. **Data Generation**: Synthetic data for TV, digital, and radio spends is generated, along with sales data that is influenced by these spends and seasonality.
2. **Exploratory Data Analysis (EDA)**: Visualizations of the sales and marketing spends over time are created. A correlation matrix is generated to understand the relationships between variables.
3. **Feature Engineering**:
   - Lagged features (previous month's spend) are added to the dataset.
   - Interaction terms between marketing spends are created.
4. **Multicollinearity Check**: Variance Inflation Factor (VIF) is calculated to check for multicollinearity. Features with high VIF are removed.
5. **Dimensionality Reduction (PCA)**: Principal Component Analysis (PCA) is applied to reduce the number of features while retaining the majority of the variance.
6. **Model Building**:
   - Linear Regression and Ridge Regression models are built to predict sales.
   - The models are trained and evaluated on a train-test split.
7. **Model Evaluation**: Model performance is evaluated using R² and RMSE (Root Mean Squared Error).
8. **Visualizations**: The actual vs. predicted sales for both models are plotted to visually compare model performance.
9. **Documentation & Results Saving**: Data and model outputs are saved in CSV files for further analysis.

## Libraries Used

- **NumPy**: For numerical computations
- **Pandas**: For data manipulation
- **Matplotlib/Seaborn**: For data visualization
- **Scikit-learn**: For regression models, PCA, and data splitting
- **Statsmodels**: For calculating Variance Inflation Factor (VIF)


## Outputs

The project generates and saves the following files:

- `marketing_data.csv`: The generated data (TV, digital, radio spends, and sales).
- `test_features.csv`: The test dataset (features after PCA transformation).
- `predictions.csv`: A file containing actual sales, linear regression predictions, and ridge regression predictions.
