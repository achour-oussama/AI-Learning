# Exercise: Analysis and Prediction on the Titanic Dataset

## Step 1: Loading and Initial Exploration
Load the `train.csv` data file into a DataFrame named `df`. Display its first rows, determine its exact dimensions (number of rows and columns), and list the names of all available variables.

## Step 2: Missing Data Diagnosis
Analyze the technical structure of your DataFrame. Identify exactly which columns contain missing values and calculate the exact number of missing values for each one.

## Step 3: Descriptive Statistics by Group
Calculate the total number of survivors and victims. Then determine the average survival rate by passenger sex and by travel class in order to observe the first influencing factors.

## Step 4: Dataset Cleaning
Handle the missing data identified in step 2:
* Replace missing values in the age column with the median value of that column.
* Replace missing values in the embarkation column with the most frequent value (the mode).
* Permanently remove the cabin column because it contains too many missing values to be usable.

## Step 5: Encoding Categorical Variables
The variables related to sex and embarkation port contain text. Convert these text variables into numeric variables so that they can be interpreted by a machine learning model.

## Step 6: Data Visualization
Use a plotting library to generate two visualizations:
* A bar chart showing the survival rate by passenger class.
* A histogram showing the passenger age distribution.

## Step 7: Train/Test Split
Separate the target variable (what we want to predict) from the explanatory variables (the passenger characteristics). Then split your dataset into two separate sets: a training set and a test set (with an 80% / 20% ratio).

## Step 8: Training and Predicting with a First Model
Create and train a logistic regression model on your training data. Then use this model to predict passenger survival on your test set.
