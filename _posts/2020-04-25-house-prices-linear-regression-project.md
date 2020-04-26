---
layout: post
published: false
title: 'House Prices Linear Regression Project '
date: '2020-04-25'
---
## Building a Multi-Variate Linear Regression Model using King County,WA House Prices Dataset Using Scikit-Learn

This project will make use of Pandas, and NumPy for the data exploration phase as well as using Matplotlib and Seaborn to form visualizations. We will then be using Scikit-Learn to model our multi-variate linear regression. We will incorporate some dummies datasets creation to deal with categorical data as well as log-transformation methodology to deal with the continuous features of the dataset.

The purpose of this project is to come up with ways in which to maximize profitability for sellers attempting to sell a home in King County,WA. We will search for actionable insights that will serve guidance to these sellers, but we need a thorough understanding of the dynamics of the housing market in order to drive our calculated decisions.

For this multiple linear regression project we will be using the kc_house_data.csv dataset. We will obtain the data using the pandas package and retrieve valuable information pertaining to the dataset using its associated modules. We will then scrub the dataset, going column per column, and inspecting for null values and dropping unnecessary columns that we won't be using in our linear regression. There will be some renaming of columns and also creation of dummies that will aid us in the process. The columns with a vast number of null values will be filled in with the median, whereas the columns with not many null values will be filled with 0's. During the exploration phase of this project, we will be creating visualizations using the matplotlib library and also seaborn. We will be creating barplots, scatterplots, and matrices. These visualizations will help us derive particular features that may be of interest to us as we move along. The trends and correlations we observe will help drive our linear regression moving forward.

After completing this initial phase of the project, we will dive right into the moduling phase of the project which encompasses building boxplots to deal with outliers. We will then rely on the powerful linear regression building tool known as scikit-learn. But, first we will need to deal with the categorical and continuous features we will be using. For the categorical features we want, we will be using dummy datasets, whereas for the continuous features, we will be employing lograrithmic transformation and min-max scaling. We will then perform the linear regression looking at valuable information such as the r^2 score, mean absolute error, and the root mean squared error, as well as the average predicted price and the average actual price for that particular model. We will conduct 3 separate trails, all the while switching up the categorical and continous features that we use. For each, we will also perform cross-validation and to test for model accuracy and looking at the significant features we used in the model that were below a p-value of 0.05.

My first recommendation to seller would be to make living space square footage their focal point 
There is a high correlation of .702 between square footage of living space and the price of the home. This is higher than any other feature that we looked at. It is evident that larger homes mandate a higher asking price. This can be seen by looking at the scatter plot on the top left. There is clearly a positive correlation with an upward trend. As square footage increases,  so does the price. It would be wise to focus on selling homes that are on the larger-end of the spectrum. This would undoubtably increase the potential commission that the seller will accrue.  

My second recommendation would be to pay particular attention to the locality of the home. House prices seem to be clustered depending on the zipcodes, which means certain zipcodes may have higher price margins than do others. We must also bear in mind that there are many factors and variables that may make one zipcode more exclusive than the other. This may be due to components such as being in close proximity to  a reputable school, fancy shopping center, or upscale restaurant. 

My third recommendation would consist of attending to the grade. The grade given by King County seems to be very influential after looking at the correlation visualizations. In general, as the grade increases, the price increases as well. Also, the grades seem to follow a normal curve. This suggests that there is nothing weird going on with how the grades are being distributed, and they propose a fair representation.  

Please take a look at the jupyter notebook file included with this repository. I include bonus recommendations and future work/research to keep in mind if you hope to expand on my work.

## Key takeways:

*1. Make living space square footage your number one feature to look out for.*

*2. Location is an extremely important feature when evaluating the price of a home.*

*3. The grade given to a home by the King County Housing Department is very influential in the price.*




