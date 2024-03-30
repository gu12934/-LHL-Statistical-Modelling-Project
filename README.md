# Final-Project-Statistical-Modelling-with-Python
![image](https://github.com/gu12934/-LHL-Statistical-Modelling-Project/assets/36687057/d28469cb-28e8-4ed8-8235-82bda1033d58)

## Project/Goals
***
In this project, we will combine and practice implementing what we have learned throughout this course, including:

* Accessing data using APIs

* Cleaning and transforming data using Python

* Loading data into a database using Python

* Performing EDA, including using both statistics and visualizations

* Identifying trends and patterns in data using statistical models

* Interpreting the results of the statistical models

***
## Files that were used

***
city_bikes.ipynb

* This notebook should be filled out based on its instructions in Part 1 of the assignment.md file and should show all of the steps you used to execute those tasks
* [link](https://github.com/gu12934/-LHL-Statistical-Modelling-Project/blob/main/notebooks/city_bikes.ipynb)
  
yelp_foursquareEDA.ipynb

* This notebook should be filled out based on its instructions in Part 2 of the assignment.md file and should show all of the steps you used to execute those tasks
* [link](https://github.com/gu12934/-LHL-Statistical-Modelling-Project/blob/main/notebooks/yelp_foursquare_EDA1.ipynb)

joining_data.ipynb

* This notebook should be filled out based on its instructions in Part 3 of the assignment.md file and should show all of the steps you used to execute those tasks
* [link](https://github.com/gu12934/-LHL-Statistical-Modelling-Project/blob/main/notebooks/joining_data.ipynb)

model_building.ipynb

* This notebook should be filled out based on its instructions in Part 4 of the assignment.md file and should show all of the steps you used to execute those tasks
* [link](https://github.com/gu12934/-LHL-Statistical-Modelling-Project/blob/main/notebooks/model_building.ipynb)

***
## Process

***
Part 1: Connecting to CityBikes API

* imported libraries
* used api endpoint and created a network url
* get the network id information
* extract station information
* parse relevant info from json into df
* print the df info for city

Part 2: Connecting to Foursquare and Yelp APIs
* Connect to the Foursquare API
* Connect to the Yelp API. This API offers similar services as Foursquare.
* Various POIs (points of interest) of your choice
* Create a DataFrame for the Yelp results and Foursquare results.
* 

Part 3: Joining Data
* Join the data from Part 1 with the data from Part 2 to create a new dataframe.
* Use data visualization to explore the data.
* Create your own SQLite database and store the data you've collected on the POIs. Put some thought into the structure of your database. We've used and created sqlite3 databases before in the activity SQL in Python. Validate your data

Part 4: Building a Model
* Build a regression model using Python’s statsmodels module that demonstrates a relationship between the number of bikes in a particular location and the characteristics of the POIs in that location.
* Interpret results. Expand on the model output, and derive insights from your model.

***
## Results
When comparing the quality of Foursquare API and Yelp API coverage for Barcelona, the Yelp API provided better details such as review count, rating, and price from a single API call based on latitude and longitude. The Yelp API was chosen to proceed with the analysis since it offers more detailed results with fewer steps compared to the Four Square API which does not give us as detailed information and insights. 

The results from the Multivariate Linear Regression Model were not very insightful. Due to the nature of the dataset, it seems like all the numerical variables are not correlated with one another.

<img width="484" alt="image" src="https://github.com/gu12934/-LHL-Statistical-Modelling-Project/assets/36687057/f15a2e29-d678-4d55-83a2-daaabb7329e0">


We can see below a few highlights from the model output:

* Adj. R-squared: This multivariate model explains only 0.7% of the variations in the data. This model doesn't seem to be a good fit.

* Prob (F-statistic): The P-value for the hypothesis test is greater than 0, so we fail to reject the null hypothesis. The independent variables do not affect the dependent variable.

* coef: We can tell from the output that the average POI price has the strongest positive impact on the number of bikes per station, whereas review_count has the largest negative impact on on the number of bikes per station.

* P>|t|: A p-value of less than 0.05 is considered to be statistically significant. This regression output shows that all p-values are >0.05. In other words,review_count, rating, and price attributes of a point of interest do not impact the number of bikes in a bike station.


## Challenges 
* it was very difficult to use the YELP api data without knowing the Bearer part of the data
* having environment variables they werent being called too easily
* converting the json data type into a dataframe
* understanding the dictionary of keys and using json normalize
* had lots of errors and debugging with the 2 API's
* reorganizing and choosing which columns are useful

## Future Goals
* I would explore the foursquare API and build a similar model and see what output i would get for the regression model
* Compare other cities and see what the overall data says with the API
* Conduct more sql series and answer more questions

## Final presentation
* https://docs.google.com/presentation/d/11QurtD-G0M9GgleXOh7RPwbe5j1P3qddLjF-bSf6fC4/edit#slide=id.g2a5d21df92d_1_64



