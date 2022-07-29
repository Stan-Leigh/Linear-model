# Project Overview

## Introduction
In this project, I implemented a Linear Regression model to predict the number of medals a country would win in the Olympic games. The Independent variables were the number of athletes participating for a country and the number of medals won by the country in the previous year.

The dataset contains olympic events from 1964 to 2016. It has 2014 rows and 9 columns. The columns are:
* team (country)
* year (olympic year)
* athletes (number of athletes representing a country for a given year)
* events (number of events the country participated in)
* age (age of the athlete)
* height (height of the athlete)
* weight (weight of the athlete)
* prev_medals (number of medals won by a country in the previous year)
* medals (number of medals won in the present year)

## Process
I started with creating a linear model by hand. I found the slope and intercept of the model using linear algebra concepts for the equation of a line. Next, I created a linear regression model with scikit learn and computed the intercept and coefficients to validate the answer I got calculating it manually. 

After checking that I was correct, I proceeded to implement the same model again but this time using the `statsmodels` package. The package allowed me access to its summary function that gave more details about the model I just created. It was here that I discovered that the other columns were not important in predicting the number of medals that a country would have, so I stuck to the two mentioned above.

Next, I proceeded to build a model that predicts number of medals won by a country. I split the data into train and test dataframes, the train data contained events that happened before 2012 and the test data had events that happened 2012 and forward.

## Results
With the slope and intercept that was calculated, we obtained an r-squared of **87.2%**. This means that 87.2% of the target variable (medals) can be explained by the predictor variables (athletes and prev_medals).

The model had an initial accuracy of **56.5%**. After transforming the target variable and running the regression model again, the accuracy got bumped to **62.9%**.
