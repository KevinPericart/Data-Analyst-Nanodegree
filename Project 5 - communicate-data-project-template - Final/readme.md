# [2017-2020/03] Bay Wheels Ride Data Exploration and Visualization


## Dataset

Bay Wheels is a regional public cicyle sharing system in the San Francisco Bay Aea, operated by Motivate in a partnetship with the Metropolitan Transportation Commission and th Bay Area Air Quality Management District.

On June 28, 2017, the system officially re-launched as Ford GoBike in a partnership with Ford Motor Company. After Motivate's acquisition by Lyft, the system was subsequently renamed to Bay Wheels in June 2019. 

Bay Wheels data is made accessible and usable by Lyft via the following link:
https://www.lyft.com/bikes/bay-wheels/system-data

**We analyzed data from January 2017 to March 2020. During this period, there were more than 5 million bicycle races in the San Francisco Bay Area.**


## Data cleaning and wrangling

We performed various data cleaning and data wrangling operations on our dataset :
- Remove usefulness columns for our analysis like 'start_station_latitude', 'start_station_longitude', 'end_station_latitude', 'end_station_longitude', 'rental_access_method', 'bike_share_for_all_trip' ;
- Remove rows without station id ;
- Turn types into datetime format ; 
- Add new columns for trip duration and trip start ; 
- Turn user_type into category format ; 
- Turn bike_id, start_station_id and end_station_id into object ; 
- Drop null values.


## Key Insights for Presentation

By analyzing this dataset we can advance different points : 
- We can observe that 78.7% of users are Subscribers and 21.3% are Customers.
- We can observe two peaks of use around 7-9 am and 4-7 pm, which corresponds to the general start and end of work schedules.
- We can see that stations 30, 15, 67, 58, 21, 3, 81 and 6 are popular.
- We can observe that the typical trip last between few seconds to 1000 seconds which corresponds to 16-17 minutes.
- We can observe a decline in activity in December which corresponds to the holiday season and winter. We can also see that activity drops in the months of April, May and June for no apparent reason.
- We can observe that customers tend to use the service much longer than subscribers. However, we must note that a bias is likely. Indeed, since there are far fewer customers thant subscribers, it is possible that the data may be somewhat biased.
- We can observe that subscribers trips follow a logical evolution according to the start and end times of work. The pattern is less marked concerning the customers, we can certainly notice some peaks of use at the hours of beginning and end of work but it not transcendent. 
- Generally speaking, the activity is more or less the same depending on whether the user is a customer or a subscriber. There are synchronous decreases in the spring during the months of April, May and June and a decrease in the winter for the month of December. Howewer, there are some asynchronous months such as the month of March, which is very active for subscribers and not very active for customers.
- We can observe that, on average, travel times are longer for subscribers than for customers. We can also observe that the different seasons of the year have little impact on the average travel time of customers. On the othe hand, the seasons have a strong impact on the use of subscribers. Thus, subscribers, move over longer periods in summer (increase from June to August) and less in winter (decrease from December to March).