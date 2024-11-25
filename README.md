# Housing Market Model

## Overview
In this project, we selected a home sales dataset from Realtor.com. The dataset provided us with information on house sales for the years 2016 to 2024. Some examples of the columns in the dataset were county names, average listing price, and average square feet; just to name a few. Using the data provided, we created a model to predict home sale prices.

## Overall Process

### Cleaning the Data
First, we read in the dataset using pandas. Next, we started cleaning the dataset by dropping unwanted columns, columns that were outliers in the dataset, and columns with NAN values. Then, we renamed the columns for easier readability. Next, we split the year/month column, dropped the combined year/month column, and reordered the columns. Finally, we exported the cleaned data into a CSV to use in the house sales model training.

### Preparing the Model
For training the model, we imported our cleaned CSV into a new notebook to use to train our model. First, we imported our dependicies, created our engine, read in our cleaned_housing_market_data csv, and loaded our dataframe into our database. Next, we created a query for our Housing_Data so if we needed to look at specific points in our data, we are about to quickly find the specific information we need. We then scaled the numeric columns. We then attempted to get_dummies from the County Names column but quickly realized that the output was too large to include in our model. We then concatinated our scaled data with our unscaled data and created our data for the model. 

### Training the Model
We found that the Linear Regression Model would be the best option for the data we prepared. We first chose our independent variable (X) as Median Sqft, Median List Price Per Sqft, and Year. Then we chose our dependent vaiable (y) as Avg Listing Price. We then trained our model and printed the shape. After fitting and predicting our model we were able to print the r2 score for our model.

### Optimization
After finding our first model only had a r2 score of 74% we attempted to optimizate our data. Our first attempt included bring the states into the data but excluding the counties. This attempt brought our r2 score to 75%. After seeing this small increase we decided to include more columns in an attempt to increase the data being fed to our model. We included the columns Median Listing Price,	Price Increased Count, and	Price Reduced Count. After training our model with this new data we found the r2 score had no significant change and had a r2 score of 74%.

## Results

Initial Attempt r2 score

![Screen Shot 2024-11-23 at 8 08 12 PM](https://github.com/user-attachments/assets/3ba0e1e7-e72b-497a-9284-0032a56b686e)

Optimization Attempt 1/ adding states

![Screen Shot 2024-11-23 at 8 09 53 PM](https://github.com/user-attachments/assets/43fd5427-aafb-4f6f-b5d3-d60aa36fe01a)

Optimization Attempt 2/ adding columns: Median Listing Price, Price Increased Count, Price Reduced Count

![Screen Shot 2024-11-23 at 8 11 26 PM](https://github.com/user-attachments/assets/dfc79dd8-ebb1-4406-b42f-a19871a0832f)

## Summary

## Resources
Dataset provided by https://www.realtor.com/. 
For visualizations published to the public. (version) Tableau 2024.3.1
https://public.tableau.com/views/Project_4_TPW/Project4Story?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
Resources provided by instructor assistance, class material, instructor video recordings, and examples given from TTC Bootcamp. Xpert Learning Assistant provided by TCC Bootcamp. Tutoring provided by TTC Bootcamp.
