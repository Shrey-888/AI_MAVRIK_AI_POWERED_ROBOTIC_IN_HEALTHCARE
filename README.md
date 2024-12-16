# AI_MAVRIK_AI_POWERED_ROBOTIC_IN_HEALTHCARE

# Project Title : Healthcare Data Cleaning and Analysis


# Group Members 
Patel Shrey, Patel Parth, Patel Manush, Aman Chordia

# Objective 

Using Python and libraries like NumPy, Pandas, and Matplotlib to:

1. Clean patient data.


2. Handle missing values effectively.


3. Analyze the cleaned data for meaningful trends in healthcare.


4. Visualize the findings through clear and insightful graphs.

## Execution step  

 1) **Importing Libraries**
    
    - import pandas as pd
    - import numpy as np
    - import matplotlib.pyplot as plt

 2) **Loading the Dataset**

    - data = pd.read_csv('healthcare_data.csv')     

3) **Displaying the First Few Rows**
    - print("First few rows of the dataset:")
    - print(data.head())
  
4) **Checking Column Names**

    - print("\nColumn names:", data.columns)
  
5) **Stripping Leading or Trailing Spaces from Column Names**

   - data.columns = data.columns.str.strip()

6) **Checking for Missing Values**

   - print("\nMissing values in each column:")
   - print(data.isnull().sum())

7) **Displaying Descriptive Statistics**

   - print("\nDescriptive statistics for the entire dataset:")
   - print(data.describe(include='all'))

8) **Handling Missing Values in the 'Cholesterol' Column**

   - if 'Cholesterol' in data.columns:
   - print("\nSummary statistics for 'Cholesterol' before filling missing values:")
   - print(data['Cholesterol'].describe())

   - data['Cholesterol'].fillna(data['Cholesterol'].mean(), inplace=True)

   - print("\nSummary statistics for 'Cholesterol' after filling missing values:")
   - print(data['Cholesterol'].describe())

9) **Grouping Data by 'HeartDisease'**

    - if 'HeartDisease' in data.columns:
    - grouped_data = data.groupby('HeartDisease').mean()
    - print("\nAverage cholesterol levels grouped by heart disease presence:")
    - print(grouped_data[['Cholesterol']])

10) **Data Visualization**

    - plt.style.use('ggplot')
    - plt.figure(figsize=(15, 10))

11) **Creating Bar Plots**

    - plt.subplot(2, 2, 1)
    - bars = plt.bar(grouped_data.index, grouped_data['Cholesterol'], color=['#1f77b4', '#ff7f0e'], alpha=0.8)

# Tools and Libraries 

    - **Python:** The primary programming language used for developing the project.

    - **Pandas:** A powerful data manipulation and analysis library for Python. It provides data structures like DataFrames, which are ideal for handling structured data, making 
      it easy to read, write, and manipulate datasets.

    - **Matplotlib:** A plotting library for Python that provides a flexible way to create static, animated, and interactive visualizations in Python. It is used in this project 
      to visualize income and expenses.

    - **CSV:** A module in Python's standard library used for reading and writing CSV (Comma-Separated Values) files. It is used in this project to store and retrieve budget 
      data.

    - **Git:** A version control system used to track changes in the project files. It allows for collaboration among team members and maintains a history of changes.

    - **GitHub:** A web-based platform for version control and collaboration. It hosts the project repository, allowing team members to share code and track issues.



# Summary of result :

- Displays the first few rows, column names, missing values, and descriptive statistics.
   Cleans column names by removing extra spaces.
- Cholesterol Analysis:
   Fills missing values in the Cholesterol column with the mean.
   Shows summary statistics before and after filling missing values.
- Heart Disease Analysis:
   Groups patients by HeartDisease (0 = No, 1 = Yes).
   Calculates averages for features like Cholesterol, Age, and BloodPressure.
- Visualizations:
   Average Cholesterol vs. Heart Disease: Bar plot to compare cholesterol levels.
   Average Age vs. Heart Disease: Bar plot to analyze age differences.
   Average Blood Pressure vs. Heart Disease: Bar plot for blood pressure trends.
   Average Cholesterol by Age Group: Bar plot to observe cholesterol across age brackets.

Challenges faced : 
