In this project, I analyzed the UK labor market over a specific period by combining multiple datasets to examine trends in unemployment, employment, and economic inactivity over the past decade. The study explores the impacts of technology, demographic shifts, austerity measures, and the COVID-19 pandemic, highlighting the complex nature of labor market changes. The goal is to provide a thorough analysis of labor market trends and contribute to the development of informed and effective policy responses.

Employment Data Analysis
Overview
This repository contains code for analyzing employment history data by age and employment status. The purpose of this code is to load, inspect, and clean the dataset to prepare it for further analysis and machine learning tasks.
Purpose
The code performs the following key functions:
1.	Loading Data: Reads the CSV file containing employment history data.
2.	Inspecting Data: Displays the first few rows and checks the dimensions of the dataset.
3.	Data Cleaning: Identifies and handles missing values to ensure data quality.
Input Format
•	CSV File: The primary input is a CSV file named Employment history by age and employment status.csv. This file should contain columns related to age and employment status.
Output Format
•	The outputs are various DataFrame inspections and visualizations that help in understanding the data.
•	The cleaned and processed DataFrame is ready for further analysis and machine learning tasks.
Description of Parameters in Defined Functions
LoadDF()
•	Purpose: Reads all CSV files in the current directory and concatenates them into a single DataFrame.
•	Parameters: None
•	Returns: A concatenated DataFrame containing data from all CSV files in the directory.
emp_age = pd.read_csv("Employment history by age and employment status.csv")
•	Purpose: Reads the specified CSV file into a DataFrame named emp_age.
•	Parameters:
o	File path: "Employment history by age and employment status.csv"
•	Returns: DataFrame containing the data from the CSV file.
emp_age.head()
•	Purpose: Displays the first five rows of the DataFrame.
•	Parameters: None
•	Returns: DataFrame (first five rows).
emp_age.shape
•	Purpose: Returns the dimensions of the DataFrame (number of rows and columns).
•	Parameters: None
•	Returns: Tuple (number of rows, number of columns).
emp_age.isnull().sum()
•	Purpose: Calculates the number of missing values in each column of the DataFrame.
•	Parameters: None
•	Returns: Series (column names and the count of missing values).
combine_df.fillna(method='ffill', inplace=True)
•	Purpose: Handles missing values by forward-filling them.
•	Parameters:
o	method='ffill': Specifies the forward fill method.
o	inplace=True: Modifies the DataFrame in place.
•	Returns: None (modifies the DataFrame in place).
Visualizations
•	Purpose: Provides various visualizations to help understand the data.
•	Functions:
o	sns.countplot()
o	pd.crosstab()
o	sns.histplot()
•	Parameters:
o	DataFrame columns for x-axis, y-axis, hue, etc.
o	Plot customization parameters like figsize, title, xlabel, ylabel, etc.
•	Returns: Plots visualized using Matplotlib and Seaborn.
Usage
1.	Clone the Repository:
sh
git clone https://github.com/yourusername/Employment-Data-Analysis.git
cd Employment-Data-Analysis
2.	Install Dependencies: Ensure you have Python and the necessary libraries installed (pandas, numpy, seaborn, matplotlib, scikit-learn, and tqdm).
pip install pandas numpy seaborn matplotlib scikit-learn tqdm
3.	 Run the Code: Execute the script to load, inspect, and clean the dataset.
python script.py


