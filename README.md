# PracticalApplication_11.1

Data Cleaning:
The data cleaning process was intensive. I dropped all features where the data was captured in other features such as state, and features that served no relevance such as ID and VIN. If the feature contained minimum null values < 5% I just dropped them from the dataset. If there were substantial nulls I replaced their value with a substitute such as unknown. I removed duplicates and dropped Harley Davidson from the manufacturer feature since it is a motorcycle company.

I cut down the amount of regions and models listed in the dataset since there seemed to be a lot of bad data on the values with low counts. I also removed any outliers from my data

Since the purpose of my model is to determine the price of a used car I significantly cut down on the years I included. Based on my charts there is a clear pattern of increase between the years 2002 and 2022. Since most cars on the road are newer than 20 years going back any further seemed only to disrupt my model. Older cars are considered classic and aren't typical in most consumer cases. Lastly, I dropped the 2023 year since its low price seemed like an outlier.


Correlation: 
It is not surprising to see odometers and age have a negative correlation with price. Also, these two features proved to be the most useful when determining the price of a used car.

Modeling:
I ran all my data through a transformer so all my categorical features were converted to numeric values and my numeric data was scaled using stadarardScaler()

I ran my data through Linear Regression and Ridge models. 

Results:
The Ridge model is the most accurate for predicting used car prices. 
