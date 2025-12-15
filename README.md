# Healthcare-Insurance-Charges-Analysis
The project is an analysis and predictive modeling of healthcare insurance charges.The analysis includes comprehensive data cleaning, exploratory data analysis (EDA) through hypothesis testing, and the development of a predictive model.

## Repository Structure
The repository structure consists of the primary code file, which contains the entire analysis and model development, alongside the three supporting datasets.This structure is completed by the README.md file, which provides an overview and guide for the project.

## Data Sources
The analysis uses three merged datasets, all found in the root directory:
 - Hospitalisation details.csv: Contains key information such as charges (the target variable), Hospital tier, City tier, and State ID.
 - Medical Examinations.csv: Includes health-related features like BMI, HBA1C, Heart Issues, Any Transplants, Cancer history, and smoker status.
 - Names.xlsx: Used to merge customer names into the main dataframe.

## Methodology & Analysis Steps
The analysis follows a standard data science pipeline:
 - Data Import and Merging: All three datasets are imported and merged into a single master DataFrame for analysis.
 - Data Cleaning: Handled missing/trivial values, specifically replacing '?' entries and converting text categories to numerical representations where appropriate.
 - Feature Engineering:Ordinal encoding was applied to Hospital tier and City tier.Conditional dummy variables were created for the top 3 most frequent State ID values.
 - Exploratory Data Analysis (EDA) & Hypothesis Testing: Statistical tests were performed to examine the relationship between charges and key categorical variables:
     - Difference in average charges across hospital tiers (Rejected Null Hypothesis).
     - 	Difference in average charges across city tiers (Accepted Null Hypothesis).
     - Difference in average charges for smokers vs. non-smokers (Rejected Null Hypothesis).I
     - ndependence between smoking and heart issues (Accepted Null Hypothesis).
 - Model Development: A Gradient Boosting Regressor was used for predicting insurance charges, showing strong performance.
 - Model Evaluation: The model was evaluated using R-squared (R^2) score and Mean Squared Error (MSE).
 - Feature Importance: Feature importances were analyzed to understand which variables most significantly influence the predicted insurance charges (e.g., smoker_yes, bmi, age).

## Installation and Setup
To run this project locally, you need Python and the necessary libraries.
### Prerequisites
    - Python 3.x
    - Jupyter Notebook or JupyterLab
### Dependencies
    - Install the required Python libraries using pip:
    - pip install pandas numpy matplotlib seaborn scikit-learn plotly openpyxl

## Core Libraries
The core libraries used in the notebook include:
 - pandas
 - numpy
 - matplotlib.pyplot
 - seaborn
 - sklearn.preprocessing.OrdinalEncoder
 - sklearn.linear_model.Ridge
 - sklearn.ensemble.GradientBoostingRegressor
 - sklearn.metrics.mean_squared_error

