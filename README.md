# **Exploratory Data Analysis on Spotify 2023 Dataset Incentive Activity**
## Submitted by: **Jihan Harvey C. Casiedo**
## Section: 2ECE-A
---
## **Background of the Activity 🖼️**
#### Spotify is a digital audio streaming platform for music, podcasts, and videos that allows users to access millions of content from creators around the globe. It has become one of the leading audio streaming platforms, having over 600 million active users as of the second quarter of 2024.
#### Exploratory Data Analysis (EDA) on a dataset featuring popular tracks from the "Most Streamed Spotify Songs 2023." will be conducted in this activity. Using Python functions, we will analyze and investigate the dataset to summarize its characteristics and develop insights into these popular tracks.
---
## **Objectives 🎯** 
### This activity aims to achieve the following:
- **Analyze** the data to identify key information.
- **Visualize** the data for better imaging and understanding.
- **Interpret** the findings to formulate meaningful insights.
---
## General Guidelines 📓
> Given instructions for the activity.
1. Familiarize with the structure of the dataset. Check for missing values and data types. Perform an initial exploration to understand the different features available.
2. Provide summary statistics on key metrics such as streams, release dates, and music attributes (e.g., BPM, danceability).
3. Use appropriate visualizations (bar charts, histograms, scatter plots) to reveal trends and patterns in the data set and ensure clarity by proper labeling. 
4. Identify correlations between different variables. Examine the relationships between streams and other musical characteristics (e.g., tempo, energy, playlists)
5. Offer insights or recommendations regarding popular tracks, artists, or musical trends based on the analysis that can be useful for understanding factors on track popularity.
#### 
---
## **Dataset 💾**
#### The dataset containing the "Most Streamed Spotify Songs 2023" can be downloaded on the *kaggle* website through this link: [Most Streamed Spotify Songs 2023](https://www.kaggle.com/datasets/nelgiriyewithana/top-spotify-songs-2023) 🔗
---
## **Activity Proper 📝**
#### Let's import the necessary libraries that we will use in our Python code.
```python
import pandas as pd
import matplotlib.pyplot as plt
```
#### The pandas library is an easy-to-use data structure and data analysis tool for manipulating and analyzing structured data, while the Matplotlib library is used for data visualization. Both of these libraries are the key tools to accomplish this activity.

#### Using the downloaded.csv file containing the "Most Streamed Spotify Songs 2023", we will load the file into spotify_data.
```python
spotify_data = pd.read_csv('spotify-2023.csv')
spotify_data
````
> Output:

![image](https://github.com/user-attachments/assets/96f72928-590c-4e52-9cb5-425b606f13fc)

#### After loading the file, it showed a Unicode Decode Error prompt. One of the reasons for this is that a different character set is encoded in the file.
#### One method we can use to load the dataset is to launch the .csv file in our device, open it in **Microsoft Excel** and export it as a .xlsx file.
#### Now, we load the file again in our code into spotify_data.
```python 
spotify_data = pd.read_excel('spotify-2023.xlsx')
spotify_data
```
>Output:

![image](https://github.com/user-attachments/assets/421826ee-8482-4a18-ac10-197348f5d1f4)

#### In this output, the dataset has a wide dataframe where some columns are hidden. We can display all the columns by changing the pandas display settings with this code:
```python
pd.set_option('display.max_columns', None)
```
#### To revert back to the original pandas display settings, this code is to be used:
```python
pd.reset_option('All')
```
---
### **Overview of the Dataset**
#### We can begin the exploratory data analysis now that we can see our dataset.
#### The size or dimension of our dataset can be known using the .shape attribute.
```python
print("Number of rows and columns:", spotify_data.shape)
```
>Output:

![image](https://github.com/user-attachments/assets/320aba75-802a-474a-ab38-89da8092d656)

#### Now we know that the dataset has **953 rows** and **24 columns**.
