# Seattle AirBNB Project

### Dashboard Link : https://public.tableau.com/views/AirBnBDashboardProject_17259158037870/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

## Problem Statement

This dashboard will help prospective property owners understand the market for AirBnB rentals in the Seattle area. By analysing average prices of rentals by zip code and size, insights can be made on if the user should start or expand their business to this territory. It will help the user understand the amount they can expect to make given the zip code and size of rental as well as what time of year has the hgihest sum of sales based on PY data.

The Seattle zip code [ 98134 ] has the highest average listing price for rentals which points to a great starting point for looking into potential properties. 

Also, the competition decreases as the room count on the property goes up. The average price of property also increases with room size, indicating that there is a shortage in the market for large sized rentals; adding another point of interest when considering investment property. 

A note as well should the investor be seeking to occupy the property for certain times in the year: Peak times of rental are from March to June and October to November. 
Consider occupying the space outside of these high traffic times to maximize profit. 



## Questions 
If someone wanted to start a BNB business, What factors would they need to know? 
1 How expensive is each Zip Code? 
2 What are the best times for him to list it if he chose to also live in the home? 
3 Bedrooms? 
4 Competition? 

### Steps followed 

- Step 1 : Collect seperate CSV files into a single XLS

- Step 2 : Load XLS into Tableau and join tables with appropriate identifier  

- Step 3 : Began bar graph creation by comparing ZIP CODE on our X axis to PRICE on the Y. We utilize color at for the zipcode and change the measure of Price to AVG.

- Step 4 : We don't want to take into account data without specifications for home size so we exclude the column which shows NULL for Room count values

- Step 5 : We finalize this by ordering the data from highest    AVG(PRICE) to lowest

![](Images/Airbnb%20zipcode%20Price.png)

- Step 6 : We continue to create another visualization to compliment the bar chart and assist the user make a decision on location by seeing the Zipcodes geographically: A Map.
We again utilize the ZIPCODE and AVG(PRICE) and switch the format to Map. 

- Step 7 : We follow the same color template as our previous chart and apply it to the Map by dragging the parameter into the Color Mark, and apply a label for the ZIP and PRICE so it is easier to understand. 

We once again remove NULL values. 

- Step 8 : Next we create a simple line graph to display the SUM of rentals over the course of time in our dataset. We use the SUM(PRICE) and  DATE from our Calendar table.

 We adjust the DATE so it displays each week to get deeper insight into timing of market. 

- Step 9 : What can be noticed is that the graph skews downward towards the end of the year, this is because of the lack of data for the start of the following year.

 We fix this by creating a filter on our DATE so only the end of 2016 is displayed. 

- Step 10: Next we want to give the user information on what size property they should invest in. To do this we create a simple bar graph that uses the BEDROOMS parameter and AVG(PRICE) and arrange it in ascending order based on Price. 

- Step 11 : Finally, I would like to provide the potential investor with an idea on the market competition for the property sizes. To accomplish this I create a table that will show how many listings there are using a count of each individual property identifier (ID) and the BEDROOMS parameter. We keep this in order of ascending bedrooms. 

- Step 12 : We combine all the worksheets made into a single dashboard so the user can get a clear and informative overview of all the information organized. This is then published to Tableau Public. 



 
 
![Publish_Message](https://user-images.githubusercontent.com/102996550/174094520-3a845196-97e6-4d44-8760-34a64abc3e77.jpg)

# Snapshot of Dashboard (Power BI Service)

![dashboard_snapo](https://user-images.githubusercontent.com/102996550/174096257-11f1aae5-203d-44fc-bfca-25d37faf3237.jpg)

 
 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard_upload](https://user-images.githubusercontent.com/102996550/174074051-4f08287a-0568-4fdf-8ac9-6762e0d8fa94.jpg)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Customers = 129880

   Number of satisfied Customers (Male) = 28159 (21.68 %)

   Number of satisfied Customers (Female) = 28269 (21.76 %)

   Number of neutral/unsatisfied customers (Male) = 35822 (27.58 %)

   Number of neutral/unsatisfied customers (Female) = 37630 (28.97 %)


           thus, higher number of customers are neutral/unsatisfied.
           
### [2] Average Ratings

    a) Baggage Handling - 3.63/5
    b) Check-in Service - 3.31/5
    c) Cleanliness - 3.29/5
    d) Ease of online booking - 2.88/5
    e) Food & Drink - 3.21/5
    f) In-flight Entertainment - 3.36/5
    g) In-flight service - 3.64/5
    h) In-flight Wifi service - 2.81/5
    i) Leg room service - 3.37/5
    j) On-board service - 3.38/5
    k) Online boarding - 3.33/5
    l) Seat comfort - 3.44/5
    m) Departure & arrival convenience - 3.22/5
  
  while calculating average rating, null values have been ignored as they were not relevant for some customers. 
  
  These ratings will change if different visual filters will be applied.  
  
  ### [3] Average Delay 
  
      a) Average delay in arrival(minutes) - 15.09
      b) Average delay in departure(minutes) - 14.71
Average delay will change if different visual filters will be applied.

 ### [4] Some other insights
 
 ### Class
 
 1.1) 47.87 % customers travelled by Business class.
 
 1.2) 44.89 % customers travelled by Economy class.
 
 1.3) 7.25 % customers travelled by Economy plus class.
 
         thus, maximum customers travelled by Business class.
 
 ### Age Group
 
 2.1)  21.69 % customers belong to '0-25' age group.
 
 2.2)  52.44 % customers belong to '25-50' age group.
 
 2.3)  25.57 % customers belong to '50-75' age group.
 
 2.4)  0.31 % customers belong to '75-100' age group.
 
         thus, maximum customers belong to '25-50' age group.
         
### Customer Type

3.1) 18.31 % customers have customer type 'First time'.

3.2) 81.69 % customers have customer type 'returning'.
       
       thus, more customers have customer type 'returning'.

### Type of travel

4.1) 69.06 % customers have travel type 'Business'.

4.2) 30.94 % customers have travel type 'Personal'.

        thus, more customers have travel type 'Business'.