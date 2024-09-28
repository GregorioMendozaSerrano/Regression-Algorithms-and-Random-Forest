# Objective
The objective of this exercise is to propose a practical application for students to develop the skills acquired in the course modules that cover the areas of Linear and Logistic Regressions, as well as Random Forest and Decision Trees.

# Statement
In the notebook, the different datasets used in the exercise are loaded.

There are three independent datasets:
- Dataset 1: used for sections 1, 2, and 3.
- Dataset 2: used for section 4 (logistic regression).
- Dataset 3: used for section 5 (decision tree).

## 1. Variable Identification
- a) Identify the categorical variables and the continuous variables.
- b) Calculate the number of records and columns in the dataframe.
- c) Calculate the number of missing values in the dataframe.
- d) Using only the information calculated up to this point: Which variables could it make sense to calculate a linear regression on?

## 2. Data Visualization
Using the matplotlib library:
- a) Create a histogram of the weight of the vehicles. What can you deduce from this histogram?
- b) Create a scatter plot between the weight and horsepower variables. What do you deduce about the relationship between these two variables?
- c) Update the dataframe using the statement “df = df.dropna()”, eliminating the missing values. What is the resulting size of the dataframe?

## 3. Linear Regression
Using the sklearn library:
- a) Take the horsepower variable as the target for linear regression. Split the dataframe into training and test sets.
- b) Perform a simple linear regression model using the weight of the vehicle as the predictor variable. Calculate the predictions of your test set and, through them, the R² of the model.
- c) Perform a multiple linear regression model using the weight of the vehicle and adding 'model_year', 'displacement', 'cylinders', 'acceleration' as the predictor variables. Calculate the predictions of your test set and, through them, the R² of the model.

## 4. Logistic Regression
You work at a real estate agency and are asked to create a model for potential homes to buy based on certain characteristics of a given dataframe. Using the scikit-learn library, and separating your dataframe into training and test sets, calculate a logistic regression model where, given a home with its longitude, latitude, median age of the area, total number of rooms, total number of bedrooms, population of the area, total number of households in the area, and median household income in the area, you can calculate whether it is feasible or not to buy it for the real estate agency. The feasibility is determined by the appraised price of the home: it must be less than 180,000 euros. For future records, this appraisal will not be available, and feasibility must be calculated based on all other characteristics. Calculate the Gini coefficient and plot the ROC curve for your model.

## 5. Decision Tree
The dataset is already loaded in the notebook. You will need to create a decision tree regressor (`sklearn.tree.DecisionTreeRegressor`) and predict the result with input values of 180, 200, 250, and 290. Repeat this exercise with the tree parameter `max_depth` set to 1, 3, and 5. Explain the reason for the difference in the prediction in the notebook.
