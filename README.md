# Foodhub Case Study
Guided EDA Project assignment DSML – MIT IDSS Course 

## The Business
FoodHub is a food aggregator that connects users, primarily students and busy professionals, with partner restaurants through a mobile app. Once an order is placed, a delivery person picks it up from the restaurant and delivers it to the customer, tracking the process via the app. FoodHub earns revenue by taking a fixed margin from each order placed through the platform.

## The Task
Analyze collected data on customer orders through their online platform and answer key business questions provided by the Data Science team, offering insights that will support the company's business improvements.

## Analyze
 1.	First look at the dataset

**Observations:**
*    There are 1898 rows and 9 columns in the data
*    Categorical features: restaurant_name , cuisine_type, day_of_week, rating<br>
     Numeric features : cost_of_the_order , food_preparation_time ,  delivery_time 
*    customer_id do not have a meaningful numeric relationship and is considered as categorical
* 	order_id also do not have a meaningful numeric relationship and is considered as categorical. But in the context of this study, it is also the primary key or unique identifier
