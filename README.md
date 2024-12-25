# ML_HousePricePred

Project Overview
This project aims to predict property sale prices using the Ames Housing dataset. 
The dataset is an enhanced alternative to the Boston Housing dataset and includes a wide range of features describing properties in Ames, Iowa. 
This project leverages data preprocessing, exploratory data analysis (EDA), and machine learning algorithms to build a robust predictive model.
________________________________________

Dataset Description

The Ames Housing dataset, compiled by Dean De Cock, contains 81 features describing various aspects of residential properties. 
The target variable is:

•	SalePrice: The property's sale price in dollars.

Key Features

•	Property Characteristics:

o	MSSubClass: Building class.

o	YearBuilt: Original construction date.

o	LotArea: Lot size in square feet.

o	Neighborhood: Physical locations within Ames city limits.

o	OverallQual: Overall material and finish quality (rated 1–10).

o	GrLivArea: Above-ground living area in square feet.

•	Basement Features:

o	TotalBsmtSF: Total square feet of basement area.

o	BsmtQual: Height of the basement.

•	Garage Features:

o	GarageCars: Garage capacity in terms of car space.

o	GarageArea: Garage size in square feet.

•	External Features:

o	Fence: Fence quality.

o	PoolQC: Pool quality.

For a complete description of all features, refer to the data description file.
________________________________________

Project Tasks

Task 1: Data Analysis

•	Performed exploratory data analysis (EDA) to understand the dataset structure and relationships between features.

•	Key steps included:

o	Visualizing correlations between numerical features and the target variable (SalePrice).

o	Handling missing data and identifying key variables with significant impact on property prices.

o	Detecting outliers using boxplots and scatterplots.

Task 2: Predictive Modeling

•	Built and evaluated various machine learning models to predict SalePrice:

o	Linear Regression

o	Ridge Regression

o	Lasso Regression

o	Random Forest Regression

o	Gradient Boosting Regressor (XGBoost)

•	Evaluation Metrics: Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), R-squared (R²).

•	Best Model: Gradient Boosting Regressor (XGBoost) provided the best performance based on RMSE and R² scores.

Task 3: Challenges and Recommendations

•	Challenges:

o	Significant missing data in features like PoolQC, Fence, and MiscFeature.

o	High cardinality in categorical features like Neighborhood.

o	Presence of outliers impacting the model's robustness.

•	Solutions:

o	Used feature engineering to impute missing values and create meaningful new features.

o	Applied one-hot encoding to handle categorical variables.

o	Normalized numerical features to improve model performance.

o	Removed or adjusted outliers to enhance model robustness.
________________________________________

Results and Recommendations

Model Comparison

![Screenshot (46)](https://github.com/user-attachments/assets/6fb68a86-38c0-4cb6-88af-ce3ceab05d85)


•	Recommended Model: XGBoost for its superior performance in terms of accuracy and generalization.
________________________________________

Key Insights:

1.	Strong Correlations:
   
o	Features like GrLivArea, TotalBsmtSF, and OverallQual have a strong positive correlation with SalePrice.

o	Outliers in LotArea and GrLivArea significantly affect predictions.

2.	Neighborhood Effect:
   
o	Properties in specific neighborhoods (e.g., NridgHt, StoneBr) have consistently higher sale prices.

3.	Year Built and Renovation:
   
o	Newer homes or those with recent renovations fetch higher prices.

4.	Feature Engineering:
   
o	Created a TotalSF feature combining GrLivArea and TotalBsmtSF for improved prediction accuracy.
________________________________________

Tools and Libraries Used

•	Data Analysis and Visualization: pandas, NumPy, Matplotlib, Seaborn

•	Machine Learning: scikit-learn, XGBoost

•	Notebook Environment: Jupyter Notebook

