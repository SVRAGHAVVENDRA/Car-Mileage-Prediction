# Car Mileage Prediction

This project involves analyzing and predicting car mileage (miles per gallon, mpg) using machine learning models. We use a dataset with car attributes to build predictive models that estimate mpg based on other factors like horsepower, weight, and origin.

## Dataset
The data is sourced from `auto-mpg.csv`, containing information on 398 cars with the following columns:

- **mpg**: Miles per gallon
- **cylinders, displacement, horsepower, weight, acceleration**: Various car attributes
- **model year, origin**: Year and region of manufacture
- **car name**: Car model name (dropped as it is non-essential for modeling)

## Steps in Data Processing and Model Training

### 1. Data Loading and Preprocessing
- **Missing Values**: The dataset has missing values in the `horsepower` column, which are replaced with the median value.
- **Categorical Encoding**: The `origin` column, initially categorical, is one-hot encoded to create separate columns for `origin_america`, `origin_asia`, and `origin_europe`.
- **Feature Scaling**: The dataset is prepared for use in various regression models.

### 2. Exploratory Data Analysis (EDA)
- **Data Summaries**: Descriptive statistics of each column help identify distributions, outliers, and missing values.
- **Bivariate Plots**: Seaborn's pairplot visualizes relationships between `mpg` and other attributes, revealing insights about variable correlations.

### 3. Model Training and Evaluation
We split the dataset into training (70%) and test (30%) sets, using the training set to fit the models and the test set to evaluate them.

- **Linear Regression Model**:
  - Trained to predict `mpg` using all other attributes.
  - Achieves an R² score of approximately 0.82 on the test data.

- **Polynomial Regression**:
  - A polynomial model with degree 2 improves the fit, achieving an R² score of 0.86 on the test data, compared to 0.90 on the training data.
  - Degree 2 is observed to provide a balance between model performance and overfitting.

- **Decision Tree Regressor**:
  - With a maximum depth of 4, the decision tree model achieves an R² score of around 0.88 on training and 0.92 on test data, indicating good performance with some overfitting control.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/SVRAGHAVVENDRA/Car-Mileage-Prediction.git
