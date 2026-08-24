# Titanic Dataset Cleaning and Machine Learning

This repository contains data cleaning, exploration, and machine learning steps for the Titanic dataset.

# Project Overview

The goal of this project is to clean the Titanic dataset and build a predictive model. 
The project prepares the data by filling missing entries based on passenger subgroups, drops unhelpful data, converts categories into clean numeric formats, and evaluates model performance using Logistic Regression.

Built With Pandas: Organizes, cleans, filters, and analyzes data tables.
           NumPy: Handles complex math calculations and manages large lists of numbers quickly.
           Matplotlib: Builds visual graphics like bar charts and graphs to see patterns.
           Scikit-Learn: Encodes text data, splits datasets, trains the machine learning model, and evaluates accuracy.
           
# Project Steps
1. Dataset Loading & Exploration
   Reads the spreadsheet file named titanic.csv into a data table called df_titanic.
   Checks the first five rows of the dataset to understand the columns.
   Looks at the data overview and sizes to identify missing entries.
   
2. Targeted Data Cleaning & Dropping Columns
   Fixing Ages by Title: Finds missing age values and fills them with the average age of passengers sharing the same title (Master, Mr, Miss, Mrs, Dr, and Ms).
   Fixing Embarked Locations: Pinpoints specific passengers ("Stone, Mrs. George Nelson" and "Icard, Miss. Amelie") to manually fill their missing embarkation ports.
   Fixing Missing Fares: Fills empty ticket prices using the middle value (median) of all ticket costs.
   Dropping the Cabin Column: Deletes the Cabin column entirely because it contains too many missing blanks to be useful.
   
3. Feature Engineering & SelectionSeparating the Target: Removes the Survived column from the main data to create the feature set (X) and saves the survival answers into a separate list (y).
   Converting Text to Numbers (Label Encoding): Translates word-based columns (like "male" and "female") into numbers using LabelEncoder for an initial numeric baseline.
   
4. Data VisualizationPlots a bar chart showing the distribution of the target variable to see how many passengers survived versus how many did not.
   
5. Custom Training FunctionEstablishes a custom reusable function named logistic(X, y) to automate model testing.Splits the data automatically: 80% for teaching the model and 20% for testing its accuracy.Uses a Logistic Regression model to learn the survival patterns.
   
6. First Model Run & EvaluationRuns the model using the initial label-encoded data.Achieves a final baseline test classification Accuracy of 82.44%.
   
7. Used One-Hot Encoding to separate multi-option word categories into clear binary numeric columns.
   Splitting the Sex Column: Transforms the text categories into distinct Sex_female and Sex_male columns.
   Splitting the Embarked Column: Breaks down the embarkation locations into three separate Embarked_C, Embarked_Q, and Embarked_S binary flags to eliminate unintended numeric ordering biases.
