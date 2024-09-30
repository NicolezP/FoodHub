# FoodHub 
EDA Project assignment DSML – MIT IDSS Course 
Refer to jupyter notebook for details on Step by Step EDA, data cleaning and visualizations

## The Business
FoodHub is a food aggregator that connects users, primarily students and busy professionals, with partner restaurants through a mobile app. Once an order is placed, a delivery person picks it up from the restaurant and delivers it to the customer, tracking the process via the app. FoodHub earns revenue by taking a fixed margin from each order placed through the platform.

## The Task
Analyze collected data on customer orders through their online platform and answer key business questions provided by the Data Science team, offering insights that will support the company's business improvements.

## Analyze 

### First look at the dataset 
*insert image 1*
*insert image 2*
### 'Not given' values in rating features
*insert image 3*
There are no null values but in ratings feature, there are values that are “Not given” which is quite a sizable chunk of the dataset<br> 
A better understanding of the statistical summary of the dataset is required to make decisions on how to treat these values. For now , we would KIV until we further explore the dataset

**Observations:**
•	There are 1898 rows and 9 columns in the data
•	There are no nulls in the dataset
•	**order_id** feature is the **unique identifier** with 1898 unique order_id matching the total number of rows , there are also no nulls in this feature.
•	rating feature of the data set has "Not given" which is actually missing customer ratings. 
•	Categorical features: restaurant_name , cuisine_type, day_of_week, rating
• Numeric features : cost_of_the_order , food_preparation_time ,  delivery_time 
•	customer_id do not have a meaningful numeric relationship and is considered as categorical

### EDA 
Below are some if the intersting insights gathered from EDA to better understand customer demand, the business partners (restaurants), what affect customer ratings and how business is different on weekndays compared to weekends

*insert image 7*
*insert image 7b*
**The top 5 most ordered cuisine_types** are : American 30.7%, Japanese 24.7%, Italian 15.7%, Chinese 11.3%, Mexican 4%

*insert image 7c*
**Top 5 restaurants** in terms of the number of orders received are: 
1. Shake Shack 
2. The Meatball shop 
3. Blue Ribbon Sushi 
4. Blue Ribbon Fried Chicken 
5. Parm 

**How days of week affect the number of orders**
*insert image 8*
There are more weekend orders which accounted for about 71.1% compared to weekday orders which accounts for 28.8%

**Top 3 customers**
*insert image 10*
The company has decided to give 20% discount vouchers to the top 3 most frequent customers. Find the IDs of these customers and the number of orders they placed
Top 3 frequent customers has customer_ids 52832 , 47440 and 83287 placed 13, 10 and 9 orders respectively
The top nth number of customers could be further analyzed to find out about their demographic to run better more relevant promotions 

**Understanding food preperation time and delivery time**
*insert image 5*
*insert image 6*
**Food Prep Time**
*   Food preparation time is almost uniform with a few peaks
*   The minimum time of preparation is 20 min and the maximum is 35 min.
**Food Delivery time** 
*   The distribution of Delivery time is left skewed.
*   There is no outliers in this variable.
*   75% of the orders are delivered in less than 28.

**How days of week affect the number of orders**
*insert image 11a*
*insert image 11b*

Observation<br>
We see higher delivery times in the weekdays mean at 28 mins compared to weekends with mean delivery times 22
There is a wider range in delivery times in the weekends
This could be something that is causing a bottleneck in fulfilling more orders in the weekends. The reason for longer delivery time can be investigated to decide on how to solve the cause. 
A few possible reasons could be the lack of man power in the delivery crew / traveling methods used by the delivery crew / non optimized travel route these within the control of the food aggregator and solutions can be put in place 


**What affect customer ratings**



### 'Not given' values in rating features
Explore the "Not given" values in rating feature to see what could have caused the missing values .
We're assuming the 'Not given' values are there completely at random so this is a case of (Missing at random). And there are several reasons reinforcing this assumption:
•	Treating misaligned values - rating: we'll want to do calculations on the rating variable, like getting the mean rating. And it is not interesting to us in this analysis to explore 'not given' as a categorical group, so we'll replace it to NaN.
•	Categorical features: restaurant_name , cuisine_type, day_of_week, rating
*insert image 3*
*insert image 9*

# WIP watch this space :) 
