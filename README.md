# Chicago Casual to Members Project
![](https://github.com/Offthecharts89/Odmandakh_Portfolio/blob/main/Images/Excel%20Logo4.png)![](https://github.com/Offthecharts89/Odmandakh_Portfolio/blob/main/Images/R%20Logo%20small.png)
### Summary
* Working with dataset with 100 million datapoints.  
* Tasked by the marketing team of Cyclistic to do an exploratory analysis of their user’s bike data. 
* Giving recommendation from my analysis of how Cyclistic can convert their casual users to full members to increase revenue, as it was previously concluded by Cyclist’s finance team that member riders are the bulk of their revenue and that they should increase the number of member riders.
* My analysis was that casual riders value fun, warm weather and the weekends. Casual riders go on longer rides on average and median. While members are more consistent. Going to work, they use it as a mode of transportation. 
* I advised the marketing team to create a weekend and summer deal. We can have them as bi-annual members or weekend member. This will create a sales funnel for casual riders to eventually become full members. 
* I gave further recommendations to market the warm weather and having fun, as casual riders value these metrics the most, using social media, their own built in app and on their bikes. 
* (For the full report you can download it above or read below)

### Overview
In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members. 
 Cyclistic’s finance analysts have concluded that annual members are much more profitable than casual riders. Moreno believes that maximizing the number of annual members will be key to future growth. Rather than creating a marketing campaign that targets all-new customers, Moreno believes there is a very good chance to convert casual riders into members. She notes that casual riders are already aware of the Cyclistic program and have chosen Cyclistic for their mobility needs. Moreno has set a clear goal: Design marketing strategies aimed at converting casual riders into annual members. In order to do that, however, the marketing analyst team needs to better understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics. Moreno and her team are interested in analysing the Cyclistic historical bike trip data to identify trends.

### Defining the Business Task
This is an exploratory analysis of Cyclistic’s biking data of its users in Chicago. The business task is to understand what the difference is between member riders and casual riders and to recommend a marketing strategy to convert casual riders into member riders. 

### Documentation of All Data Sources Used 
All data was provided by Motivate International Inc. Motivate gathers data for all rides each month and stores it as a csv file. I downloaded the data for the last 12 months in 12 csv files, one for each month with varying size. The type of data gathered is 
![](https://github.com/Offthecharts89/Odmandakh_Portfolio/blob/main/Images/calctable.png)

I have been given permission to use the data provided and after an overview the data is clear of bias and ethical to use. No personal information about users was provided so there is no need to scrub the data.
I also in the process of aggregating the data into one data frame. I  named each of the files by month as a separate variable called data source. This was to help me identify if there are any problems with the data I know which file the error is occurring and I will later use the additional variable I created to do a monthly analysis. 

### Documentation of Any Cleaning or Manipulation of Data 
Considering the business task I have chosen to use R as it is able to handle the amount of data. With 5.5 million observations and 14 variables tools like excel cannot handle this large dataset.  Furthermore, it has an inbuilt visualization tool that I can use to show case the data that SQL does not provide. Using the started at and ended at variables. I performed two initial calculations to find out the ride length in time and the day of the week that the ride occurred. This uncovered the fact that in some instances the started at and ended at data was input incorrectly, the times were switched.  I had to convert the time into a number and use the abs() function to convert all negative numbers to positive. I would then transform the data into a days : hours : minutes : seconds format so that it could be easily understood at a glance. 
After manipulating the data to make sure for data integrity, I checked for duplicates with the unique() function on ride id to make sure that I was not using the same observation twice. All observations had a unique ID and so I can say there were no duplicates. I aggregated all of my clean data into one data frame and started my analysis. 

### Aggregated the data and performed calculations to find relationships or trends.
I had decided for my analysis that I would first do an initial analysis of all the data to have a better understanding as a whole then split the data into member and casual rides.  I performed an initial calculation of the average, median and max rides for the whole data set. This would be used as a bench mark for when the data is split. I would then brake the data down into  number of rides in months and weekdays to discover trends or relationships within the data. 

#### Visualized the data in weeks and months. Found a trend that there would be a surge in rides over the weekend and in the summer months 

![](https://github.com/Offthecharts89/Odmandakh_Portfolio/blob/main/Images/Weekday%20Total.png)

As we can see in the graph there is a marked increase in the number of rides over the weekend. I believe this is an key opportunity for marketing and something that Cyclistic could focus on to offer value to their customers. We can also see a similar trend in the monthly data.

![](https://github.com/Offthecharts89/Odmandakh_Portfolio/blob/main/Images/Month%20Total.png)

Again we see a surge another trend showing in our data. People go on more rides during the summer months and on the weekend. I would suggest to create a weekend and monthly package for casual riders. This is to let casual riders become half members in peak time so that the gap in commitment between half members and full members is less than casual and members. This can act as a sales funnel so that our customers can still enjoy our bikes but also make it easier for them to make the transition from casual riders to full riders.

However you may say that we don’t know if it is primarily the members or the casual riders that are causing the surge in rides. I split our data to casual riders and member riders. Then performed some quick calculations to get an overview when we compare them both together. 

### Compared casual riders to member riders to understand the difference between them.
![](https://github.com/Offthecharts89/Odmandakh_Portfolio/blob/main/Images/Calc.png)

As we can see from our graph casual riders ride for longer in all metrics. This helps my hypothesis that casual riders are looking to have fun while member riders use their bikes for their daily routine going from point A to point B with no side tangents. Casual riders are motivated to having fun! 

#### Looking at the number of casual riders compared to memeber riders 
![](https://github.com/Offthecharts89/Odmandakh_Portfolio/blob/main/Images/Pie%20Chart.png)

For all of our rides in the past year, 45% are casual rides. There is a big market for this and having a our marketing be targeted at the 45% of casual riders will help us not waste funds on the 55% of riders that are already members.

### Comparing Casual Riders vs Members Riders on Weekdays
![](https://github.com/Offthecharts89/Odmandakh_Portfolio/blob/main/Images/Casual%20Weekday.png)

Again with causal rider we see the same trend of rides peaking in the weekend.
![](https://github.com/Offthecharts89/Odmandakh_Portfolio/blob/main/Images/Member%20Weekday.png)

 The interesting observation with member riders is that they peak on Tuesday and Wednesday but then gradually decrease. The weekend has the lowest number of member riders.
 
 ![](https://github.com/Offthecharts89/Odmandakh_Portfolio/blob/main/Images/Member%20vs%20Casual%20Weekday%20small.png)

Looking at casual and members rides directly we can see that members riders are much more consistent in their routines while casual riders really look forward to the weekend to use their bikes. With casual riders even surpassing member riders during the weekend and reaching the highest high in terms of number of rides. I can confidently say that creating a weekend package deal will be primarily targeting casual riders and leading them to become half members.

### Comparing Casual Riders vs Members Riders by Month
![](https://github.com/Offthecharts89/Odmandakh_Portfolio/blob/main/Images/Casual%20vs%20Member%20Month.png)

Again we can see the same story. Casual Riders are much more seasonal in their behaviour. The weather plays a big factor for them as casual rider dip below the bar in the winter months and even pass the bar in the summer months. While member riders are much more consistent. They stay within the bars for most of the year. I can also confidently say that creating a summer package for casual riders to enjoy will boost the companies revenue by creating bi-annual members that can lead onto to becoming full members in the future. 

## Top Three Recommendations

* Create a weekend and bi-annual members package for casual riders to use. This will affectively make them half members.
* Market their riders for fun and warm weather. Casual riders seem to value these metrics the most.
* Use social media, their own built in app and their bikes to promote the deal. 
