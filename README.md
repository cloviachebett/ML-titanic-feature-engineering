Titanic Dataset Cleaning and Machine Learning.
This repository contains data cleaning, exploration, and machine learning steps for the Titanic dataset.AuthorClovia ChebetProject.
The project prepares the data by filling missing entries based on specific passenger subgroups and converts text columns into numbers so a machine learning model can process them.
Built With Pandas: Organizes, cleans, filters, and analyzes data tables.
           NumPy: Handles complex math calculations and manages large lists of numbers quickly.
           Matplotlib: Builds visual graphics like bar charts and graphs to see patterns.
           Scikit-Learn: Encodes text data, splits datasets, and trains the machine learning model.
  Project Steps
  1. Dataset Loading & Exploration Reads the spreadsheet file named titanic.csv into a data table called df_titanic.
  2. Checks the first five rows of the dataset to understand the columns.
  3. Looks at the data overview and sizes to identify missing entries.
  4. Targeted Data Cleaning
      Fixing Ages by Title: Finds missing age values and fills them with the average age of passengers sharing the same title (Master, Mr, Miss, Mrs, Dr, and Ms).
      Fixing Embarked Locations: Pinpoints specific passengers ("Stone, Mrs. George Nelson" and "Icard, Miss. Amelie") to manually fill their missing embarkation ports.
      Fixing Missing Fares: Fills empty ticket prices using the middle value (median) of all ticket costs.
  5. Feature Engineering & Selection
     Separating the Target: Removes the Survived column from the main data to create the feature set (X) and saves the survival answers into a separate list (y).
     Converting Text to Numbers: Uses a tool called LabelEncoder to translate word-based columns (like "male" and "female") into numbers so the computer can process them.
  6. Data VisualizationPlots a bar chart showing the distribution of the target variable to see how many passengers survived versus how many did not.
  7. Machine Learning TrainingSplits the data into two groups: 80% for teaching the model and 20% for testing its accuracy.Uses a Logistic Regression model to learn the survival patterns.
     Tests the model on the remaining data and prints out a final accuracy score percentage.
