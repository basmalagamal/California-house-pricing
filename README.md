California-Housing

🏡 California House Price Prediction
This project analyzes California housing data to predict median house value using regression models.
It involves data cleaning, preprocessing, feature engineering, and machine learning modeling.

📂 Dataset

Source: [California Housing Prices (Kaggle)
](https://www.kaggle.com/datasets/camnugent/california-housing-prices)
Shape: ~20,640 rows × 10 columns

Target Variable: median_house_value (continuous numeric)

Key Columns:

longitude, latitude: Geographic location.

housing_median_age: Median house age in block.

total_rooms, total_bedrooms: Housing composition.

population, households: Demographic information.

median_income: Median income (scaled).

ocean_proximity: Categorical feature (<1H OCEAN, INLAND, NEAR BAY, etc.).

median_house_value: Target column.

🛠️ Project Workflow

Data Cleaning

Handled missing values in total_bedrooms (imputed with median).

Removed extreme outliers in house values.

Exploratory Data Analysis (EDA)

Distribution plots for income, age, and prices.

Correlation heatmap of numeric variables.

Geographic scatterplots (longitude × latitude vs house value).

Feature Engineering

Created new features:

bedroom_ratio = total_bedrooms / total_rooms

rooms_per_household = total_rooms / households

population_per_household = population / households

Encoded categorical variable ocean_proximity (One-Hot Encoding).

Preprocessing

Scaled numerical features using StandardScaler.

Handled skewness with log transformations (population, rooms).

Data Splitting

Train-test split: 80% training, 20% testing.

🤖 Models & Results

Linear Regression → 64% R²

Random Forest + GridSearchCV → 82% R²
