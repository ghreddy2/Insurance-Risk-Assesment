# Insurance-Risk-Assesment

### Problem Statement:
  A vehicle insurance company wants to asses the risk assosiated with its customers who would claim the insurance amount for their vehicles.
  
### Analytical Statement:
  The risk assosiated is classified as three classes- High, Medium, Low based on some features like the Driving_Frequency, Vehicle_condition, Market_value, No.of_claims, etc. Asthis is a classification problem, I tried classification models to fit the data.
  
### Data collection:
  I collected the data fromo a trusted source who is an Information architect at an MNC company which provides solutions for insurance companies.
  
I imported the data using the pandas package to load our excel file.pandas helps us by allowing the data manipulation functions with the numpy record arrays.

I checked for the shape of the dataframe which has 2000 rows and 16 columns which are considered for the insurance business.

### EDA
The first thing done is to identify the datatype of each attribute at which we found only 5 numerical and the rest are categorical attributes.

I checked for the missing values, luckily we donot have any missing values by which we can understand that the data we have helps to solve the problem more accurately. If we are having any missing values,we would have to impute them by various methods.

I checked for unique value records in each categorical attribute to understand for the process of feature engineering.

Then I started to explore through the data by doing bivariate analysis between the dependant and the independant variables.
    I found that almost 63% of its customers are associated with medium risk.
    When I tried to find the relation for risk profile and the driving frequency, highest number of customers are at Medium risk who drive occassionally.
    At the driving purpose, 50% of the high risk customers use their vehicle for racing purpose.
    Customers who have no driving experience are considered as high risk customers.
    
Feature engineering(to convert the categorical variables as numerical for the better fit of the model) is done on categorical variables. For less unique_values, we had done manual encoding and the others are done with the help of LabelEncoder.

With the help of Seaborn, a data visualization library based on matplotLib to check the distributiion of age.

After transformation, I tried to find the correlation with the help of correlation matrix with the help of heatmap. To get us an information which attributes are correlated.

The risk profile has a positive correlation with driving_purpose, driving_experience, age, gender and topography.

### Model building
  The data is split in a manner such that 70% is for train and the 30% is for test.
 
I observed that the model is overfitting the data, then searched for the feature importances and found that some of them are contributing very less to the target. Hence I dropped them.

Three types of classifiers are fit on the data to check which gives us the best solution.

The model can be used as an AI model to predict the risk associated with the new coming customers.
