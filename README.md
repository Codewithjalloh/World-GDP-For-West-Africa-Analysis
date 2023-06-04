# World-GDP-For-West-Africa-Analysis

Here's an explanation of the code:


import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load the data from CSV file
df = pd.read_csv('dataset.csv')
This code imports the necessary libraries (Pandas, Seaborn, and Matplotlib) and loads the dataset from a CSV file.

python
Copy code
# Filter data for countries in Africa
africa_df = df[df['Country Name'].str.contains('Africa')]
This code filters the data to include only the rows where the 'Country Name' column contains the string 'Africa'. It creates a new DataFrame called 'africa_df' that contains the filtered data.


# 1. What are the unique country names in Africa?
unique_countries = africa_df['Country Name'].unique()
print("Unique country names in Africa:", unique_countries)
This code finds the unique country names in the 'Country Name' column of the 'africa_df' DataFrame and stores them in the 'unique_countries' variable. It then prints the unique country names in Africa.


# 2. What is the maximum value recorded in Africa?
max_value = africa_df['Value'].max()
print("Maximum value in Africa:", max_value)
This code finds the maximum value in the 'Value' column of the 'africa_df' DataFrame and stores it in the 'max_value' variable. It then prints the maximum value recorded in Africa.


# 3. How many unique country codes are there in Africa?
unique_country_codes = africa_df['Country Code'].nunique()
print("Number of unique country codes in Africa:", unique_country_codes)
This code calculates the number of unique country codes in the 'Country Code' column of the 'africa_df' DataFrame and stores it in the 'unique_country_codes' variable. It then prints the number of unique country codes in Africa.


# 4. What is the average value in Africa?
average_value = africa_df['Value'].mean()
print("Average value in Africa:", average_value)
This code calculates the average value in the 'Value' column of the 'africa_df' DataFrame and stores it in the 'average_value' variable. It then prints the average value in Africa.


# 5. How many years of data are available for countries in Africa?
years_available = africa_df['Year'].nunique()
print("Number of years available for countries in Africa:", years_available)
This code calculates the number of unique years in the 'Year' column of the 'africa_df' DataFrame and stores it in the 'years_available' variable. It then prints the number of years available for countries in Africa.

# Bar plot: Value by Country in Africa
plt.figure(figsize=(10, 6))
sns.barplot(data=africa_df, x='Country Name', y='Value')
plt.title("Value by Country in Africa")
plt.xlabel("Country Name")
plt.ylabel("Value")
plt.xticks(rotation=45)
plt.show()
This code creates a bar plot using Seaborn to visualize the value by country in Africa. It uses the 'africa_df' DataFrame as the data source and plots the 'Country Name' on the x-axis and the 'Value' on the y-axis. The plot is then customized with a title, x-label, y-label, and rotated x-axis tick labels. Finally, the plot is displayed using plt.show().

The remaining code follows a similar pattern, addressing the remaining questions in the same manner and creating visualizations using Seaborn and Matplotlib.




