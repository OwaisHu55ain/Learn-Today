# Exploratory Analysis of Roller Coaster Data

```python

 # Import necessary libraries
import os
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

 # Set style for matplotlib plots
plt.style.use("ggplot")

 # Set pandas options
pd.set_option("display.max_columns", 100)

 # Print current working directory
print("Current working directory:", os.getcwd())

 # Change directory to the specified location
os.chdir("C:/Users/zakir/Desktop")

 # Load data from CSV into DataFrame
df = pd.read_csv("coaster_db.csv")

 # Display basic information about the DataFrame
print("Shape of the DataFrame:", df.shape)
print("Columns of the DataFrame:", df.columns)
print("Data types of the columns:")
print(df.dtypes)

 # Select relevant columns for analysis
df = df[['coaster_name', 'Location', 'Status', 'Manufacturer', 'year_introduced',
         'latitude', 'longitude', 'Type_Main', 'opening_date_clean', 'speed_mph',
         'height_ft', 'Inversions_clean', 'Gforce_clean']].copy()

 # Display the shape of the DataFrame after selection
print("Shape of the DataFrame after column selection:", df.shape)

 # Convert date columns to datetime format
df["opening_date_clean"] = pd.to_datetime(df["opening_date_clean"])

 # Convert year column to numeric format
df["year_introduced"] = pd.to_numeric(df["year_introduced"])

 # Rename columns for clarity
df = df.rename(columns={'coaster_name': "Coaster_Name", 'year_introduced': "Year_Introduced",
                        'latitude': "Latitude", 'longitude': "Longitude",
                        'opening_date_clean': "Opening_Date_Clean", 'speed_mph': "Speed_mph",
                        'height_ft': "Height_ft", 'Inversions_clean': "Inversion",
                        'Gforce_clean': "Gforce"})

 # Handle missing values
print("Number of missing values per column:")
print(df.isna().sum())

 # Remove duplicate entries based on specific columns
df = df.loc[~df.duplicated(subset=["Coaster_Name", "Location", "Opening_Date_Clean"])].reset_index(drop=True).copy()

 # Display the shape of the DataFrame after removing duplicates
print("Shape of the DataFrame after removing duplicates:", df.shape)

 # Visualize data

 # Plot top 10 years for roller coaster introduction
ax = df["Year_Introduced"].value_counts().head(10).plot(kind="bar", title="Top 10 Years for Roller Coaster Introduction")
ax.set_xlabel("Year Introduced")
ax.set_ylabel("Count")
plt.show()

 # Plot histogram and kernel density estimate for coaster speed
fig, axs = plt.subplots(1, 2, figsize=(12, 5))
df["Speed_mph"].plot(kind="hist", bins=20, title="Coaster Speed (mph)", ax=axs[0])
df["Speed_mph"].plot(kind="kde", title="Coaster Speed (mph)", ax=axs[1])
plt.show()

 # Plot scatter plot for coaster speed vs height
plt.scatter(x="Speed_mph", y="Height_ft", data=df)
plt.title("Coaster Speed vs Height")
plt.xlabel("Speed (mph)")
plt.ylabel("Height (ft)")
plt.show()

 # Plot pairplot for selected variables with hue based on 'Type_Main' column
sns.pairplot(df, vars=["Year_Introduced", "Speed_mph", "Height_ft", "Inversion", "Gforce"], hue="Type_Main")
plt.show()

 # Calculate correlation matrix
df_corr = df[["Year_Introduced", "Speed_mph", "Height_ft", "Inversion", "Gforce"]].corr()

 # Plot heatmap for correlation matrix
sns.heatmap(df_corr, annot=True)
plt.title("Correlation Matrix")
plt.show()

 # Group by location and calculate average coaster speed for locations with at least 10 coasters
location_speed_mean = df.query("Location != 'Other'").groupby("Location")["Speed_mph"].mean()
location_speed_mean = location_speed_mean[location_speed_mean >= 10].sort_values()
location_speed_mean.plot(kind="barh", figsize=(12, 5), title="Average Coaster Speed By Locations")
plt.xlabel("Average Coaster Speed (mph)")
plt.ylabel("Location")
plt.show()

```
