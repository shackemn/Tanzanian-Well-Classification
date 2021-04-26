# Tanzanian Well Classification

Author: Micah Shackelford



## Business Case

Tanzania has had a problem with available water to the general populace for many years.

The Tanzanian government has hired us to figure out a way to imporve methods in identifying non-functioning water wells.

We will be trying to detect which key features will help up identify the status of these wells.

### The Data

Data comes from waterpoints all across Tanzania

60,000 different waterpoints are included and are classified into “functioning”, “non functioning”, and “needs maintenance”

Data includes many different features of the wells including geographic location, water source, water quality, pump type, construction year, etc.




### Exploration
Taking a closer look at the data, We classified our features into continuous and categorical features. Then we looked at visualizations
to explore their linear relationship to price. We also looked at multicolinearity and removed  few features which would cause problems with our model.

Something noteworthy found was the mean sales price of waterfront homes was over three times greater than the average mean price of other homes. This can be observed in the visualization below.

![Location Map.png](https://github.com/shackemn/Tanzanian-Well-Classification/blob/main/Location%20Map.png)

We also used scikit learn's One Hot Encoder for our categorical features


## Models

We used three different models for this project. Random Forest, XGBoost, and Decision Tree

XG boost was our best model with an accuracy score of 74.65%

The test data had an accuracy score of 81.52%, so our model did overfit a little bit. 

Our model showed that the most important features were, amount_tsh, region_code, construction_year, and population

![Feature Importance2.png](https://github.com/shackemn/Tanzanian-Well-Classification/blob/main/Feature%20Importance2.png)




## Recommendations

Look into these water points with low amounts of access to water. Why are these not getting the water they need? If we can give these wells better access to water, we should be able to solve a large portion of the problems.

There is definitely a pattern with location and the status of the wells. We saw this in the visualizations and in our models. Try to find why this is. Is it a problem with the local regulations or something larger?

The population surrounding the wells also seems to be important. A lower population probably means that there are less regulations and maintenance. These wells are still needed though. The government needs to focus on getting these wells back online.

## Future Work

We focused solely on the functioning and non functioning wells, since it was the more pressing issue. In the future we need to also better recognize which wells need maintenance, so the gap does not increase.

This data only go up to 2013. Update the data with more recent well information.



