# Uber-Fare-
This study will give a prediction on the fare pricing of Uber in future transactions. The company is the largest in the world and handles thousands, if not millions of customers, on a regular basis. The firm will still require effective data management to be sure of innovating and getting the right price.

# Data Cleaning and Transformation
Loading and Initial Inspection:

The dataset loaded successfully. Preliminary inspection of the columns revealed variables with missing values. These were cleaned by dropping the rows containing them.
Rename and Remove Columns:

You renamed the column Unnamed: 0 as Id and removed the column for duplicate keys.
Convert to Date and Time:

The column pickup_datetime was changed to datetime format, which is essential when time-based analysis should be run.

Added a 'distance_km' column for calculating distances between the pickup and dropoff points using the Haversine formula. Data Statistical Summary: You gave a descriptive statistics representation that returned to show extreme outliers in 'fare_amount', 'pickup_longitude', 'pickup_latitude', 'dropoff_longitude', 'dropoff_latitude', and 'passenger_count'. Visualizations Distance: Box plots and histograms indicate that most rides are short, less than 5 km. Fare Amount: Skewed with outliers; most fares are between $5 and $20.
Passenger Count: Most rides have 1-2 passengers, with some rides reaching as high as 8 passengers. 
Mean Fare by Passenger Count:

You have looked at fare amounts with respect to passenger counts and found large discrepancies. These were formally tested through hypothesis testing. 
Monthly and Daily Ride Counts:

Monthly: The number of rides remains very consistent, but there are fewer rides during summer months.
Daily: There is a higher number of rides during the weekdays with dips during the weekends. 
Revenue Analysis:

By Day: Fridays have highest revenue and Mondays the lowest.
By Month: Trends in revenue follow trends in ride counts: less in summer months
Hypothesis Testing
Fare Amount and Passenger Count
Conducted an ANOVA test that returns there is a significant difference in the average Fare Amount based on Passenger Count. So reject the null hypothesis
Outlier Detection and Preparation for Modeling
Outliers:
Box plot identifies outliers in fare_amount, distance_km, and passenger_count
Duplicates and missing values:

You had checked for no duplicates and dealt with missing values earlier.
Next Steps
Dealing with outliers in fare_amount and distance_km can be more systematic. Either trimming, or some transformation, or use of robust methods can be useful.
Feature Engineering
Temporal Features: Add more temporal features like time of day or day of the week to gain further insights.
Interactions: One may look at various interactions between the features like distance_km * passenger_count.
Modeling:

Regression Analysis: The next step will be the fitting of a linear regression model or other regression techniques such as Lasso and Ridge, against fare_amount.
Evaluation Measure will use Cross-validation. Evaluation metrics will include RMSE and MAE; R² is also to be included.
Geospatial Analysis:

Plot pickup and dropoff locations in maps to find spatial patterns and anomalies.
