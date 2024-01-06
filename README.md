### Capstone Project Descriptions 
### Task 1: Data Cleaning
### Project Overview
In this intriguing project, you analyze your electricity usage history to determine the optimal contract for minimizing your annual electricity cost. The dataset, provided in the "data_cleaning.xlsx" file, contains various challenges that require your attention.
### Objectives
1.	Perform comprehensive data cleaning techniques.
2.	Implement multiple-choice questions marked in the dataset.
3.	Data Cleaning and Analysis
### Dataset Overview
The provided Python code is focused on data cleaning and analysis for a dataset related to electricity usage. The dataset is loaded from an Excel file named "data_cleaning.xlsx" and contains information about electricity usage, including time, electricity consumption, and date.

### Steps in the Code
1. Initial Data Loading and Cleaning
The dataset is initially loaded using pd.read_excel.
Column names are assigned to the dataframe for better readability.
Regular expressions are utilized to extract information such as time, electricity usage, and date from the 'col' column.
2. Date and Time Formatting
The 'date' column is converted to a datetime format for better handling.
The 'week_name' column is created to store the day of the week corresponding to each date.
The 'hour' column is extracted from the 'time' column, which is converted to datetime format.
3. Contract Data
Contract information is provided in a Python dictionary and then converted to DataFrames for 'No Flex', 'Monthly Flex', and 'Hourly Flex'.
Each DataFrame is written to a separate Excel file.
4. Analysis Questions
The code addresses specific questions related to electricity usage:
Average hourly electricity usage.
Average electricity usage per hour in February.
Day of the week with the highest average usage.
Highest amount of electricity used in a continuous 4-hour period.
Annual cost of electricity under the "Monthly Flex" contract.
Lowest annual cost among three different contracts.
Answering Analysis Questions
Average Hourly Electricity Usage:

The code calculates the average hourly electricity usage by converting the 'electricity_usage' column to numeric and then finding the mean.
Average Electricity Usage per Hour in February:

The code filters the dataset for February, calculates the average electricity usage per hour, and provides the result.
Day of the Week with the Highest Average Usage:

The code introduces a new column 'day_of_week' and groups the data by day to find the day with the highest average electricity usage.
Highest Amount of Electricity Used in a Continuous 4-Hour Period:

The code sorts the dataset by date and hour, creates a rolling sum column over a 4-hour window, and finds the maximum value in the rolling sum.
Annual Cost of Electricity under the "Monthly Flex" Contract:

The code merges the dataset with the 'Monthly Flex' contract information, calculates the monthly cost, and sums the monthly costs to get the total annual cost.
Lowest Annual Cost Contract:

The code calculates the annual cost for each contract and identifies the contract with the lowest annual cost.
Conclusion
The code provides a comprehensive analysis of electricity usage, answering specific questions related to average usage, monthly costs, and contract comparisons. It demonstrates the use of regular expressions, datetime manipulation, and contract data integration for data cleaning and analysis.

Note: The code assumes the correctness and consistency of the provided dataset. Adjustments may be needed for real-world scenarios with diverse and potentially erroneous data.


### Task 2: McKinsey&Company Prohack
### Intergalactic Development Index Prediction
### Overview
This Python code focuses on predicting the Intergalactic Development Index (IDI) using machine learning techniques. The IDI is a composite index that measures the overall development of a galactic society based on various socio-economic factors. The code includes data loading, exploration, preprocessing, feature engineering, missing value imputation, scaling, encoding, and model training.

### Dataset
The dataset consists of two CSV files: 'train.csv' and 'test.csv'. The 'train.csv' file contains the training data with features and the corresponding IDI values. The 'test.csv' file contains the test data with features for which predictions need to be made.

### Steps in the Code
1. Data Loading and Exploration
Importing necessary libraries such as pandas, numpy, matplotlib, seaborn, xgboost, and sklearn.
Reading the training and test data into Pandas DataFrames.
Displaying basic information about the dataset, such as Python version and OS environment.
Exploring the structure of the training data, including the first few rows, summary statistics, and the number of unique galaxies and years.
2. Data Preprocessing
Concatenating the training and test DataFrames for preprocessing.
Dropping irrelevant columns ('galactic year', 'galaxy', and 'y') for initial analysis.
Using the missingno library to visualize missing values in the dataset.
Removing rows with missing values and concatenating cleaned DataFrames into 'total_df'.
Calculating the correlation matrix and plotting a heatmap to identify highly correlated features.
Iterating through columns to identify correlated features, training ElasticNet models, and saving the models using pickle.
Imputing missing values in the target column using the trained ElasticNet models.
3. Feature Engineering and Imputation
Creating new train and test DataFrames after imputation.
Joining the original 'galactic year', 'galaxy', and 'y' columns to the new train DataFrame.
Joining the original 'galactic year' and 'galaxy' columns to the new test DataFrame.
Concatenating new train and test DataFrames into a single DataFrame 'df'.
Sorting the DataFrame by 'galaxy' and 'galactic year'.
Interpolating missing values using linear interpolation and filling remaining missing values with mean for each galaxy.
4. Scaling and Encoding
Selecting numeric columns based on specified column names.
Scaling numeric columns using the RobustScaler from scikit-learn.
Creating a categorical target variable based on specified thresholds.
Encoding the categorical column 'galaxy' using CatBoostEncoder from the category_encoders library.
5. Model Training and Evaluation
Training an initial XGBoost regressor and evaluating its performance on a validation set.
Performing hyperparameter tuning using GridSearchCV to find the best set of hyperparameters.
Training the XGBoost regressor with the best hyperparameters.
Analyzing feature importances and visualizing them using a bar plot.
Evaluating the model's performance using cross-validation and calculating mean and standard deviation of the scores.
Making predictions on the validation set and calculating the Mean Squared Error.
6. Conclusion
Summarizing the key steps and outcomes of the analysis.
Providing a note about assumptions and potential customization based on the characteristics of the actual dataset.
Note
This analysis assumes that the features in the dataset are relevant for predicting the Intergalactic Development Index. Customization may be necessary depending on the specifics of the dataset being used.


