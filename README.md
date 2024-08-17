# Flight Price EDA and Feature Engineering

This project performs Exploratory Data Analysis (EDA) and feature engineering on a flight price dataset.

## Data Loading and Initial Exploration

1. Imported necessary libraries: pandas, numpy, matplotlib, seaborn
2. Loaded training data from 'Data_Train.xlsx' and test data from 'Test_set.xlsx'
3. Combined training and test data into a single dataframe for analysis

## Date and Time Feature Engineering

1. Split 'Date_of_Journey' into separate 'Date', 'Month', and 'Year' columns
2. Converted these new columns to integer type
3. Removed the original 'Date_of_Journey' column

## Arrival Time Processing

1. Extracted hour and minute from 'Arrival_Time'
2. Created new columns 'Arrival_hour' and 'Arrival_min'
3. Converted these new columns to integer type
4. Removed the original 'Arrival_Time' column

## Departure Time Processing

1. Extracted hour and minute from 'Dep_Time'
2. Created new columns 'Dept_hour' and 'Dept_min'
3. Converted these new columns to integer type
4. Removed the original 'Dep_Time' column

## Handling Categorical Variables

1. Mapped 'Total_Stops' to numerical values (e.g., 'non-stop' to 0, '1 stop' to 1, etc.)
2. Removed 'Route' column as it contained similar information to 'Total_Stops'
3. Used LabelEncoder to encode 'Airline', 'Source', 'Destination', and 'Additional_Info' columns

## Duration Processing

1. Extracted duration in hours from 'Duration' column
2. Removed rows with invalid duration ('5m')
3. Converted duration to integer type
4. Removed original 'Duration' column

## Final Steps

1. Applied one-hot encoding to 'Airline', 'Source', and 'Destination' columns using pd.get_dummies()

This EDA process cleaned the data, engineered new features, and prepared the dataset for machine learning modeling.
