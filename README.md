**Insights and Conclusions**



1. The columns of `'is_cutoff', 'cutoff_factor', 'cutoff_timestamp', 'segment_factor', 'factor' `carry no definition so we try to drop them
2. The categorical columns having no data are imputed using the most frequent strategy.
3. Grouping the data by segment gives us the cum sum of time and distance giving actual time for each segment.
4. Creating a dictionary for group by aggregation helps to easily manage the group by output for each column.
5. Again grouping by the trip_uuid helps to lastly gain cumulative data for trip wise.
6. Creating features like time differences helps to gain deeper insights.
7. Splitting the columns of source and destination name into state, city, place and code helps to gain granularity.
8. Almost all numerical columns have outliers.
9. One hot encoding of the data and route_type helps to see more relation among data.
10. Almost all columns have right skewed data. But it is not log normal data.
11. The columns of particular time and distance (like segment time and distance) have a higher correlation.
12. It is Statistically proved with hypothesis testing that the average actual time is same as the avg osrm_time.
13. It is Statistically proved with hypothesis testing that the average actual time is greater than the average segment actual time.
14. It is Statistically proved with hypothesis testing that the avg osrm distance is greater than avg segment avg osrm segment distance.
15. It is Statistically proved with hypothesis testing that the avg osrm time is greater than the average segment osrm time.
16. Almost 60% of trips are of the Carting Route type.
17. Most of the trips are created during the middle of month, around the 15-21 date.
18. The State with the most destination trips is Maharashtra.
19. The City with the most destination trips is Bengaluru.
20. The Place with the most destination trips is Bilaspur.
21. The State with the most Source trips is Maharashtra.
22. The City with the most Source trips is Gurgaon.
23. The Place with the most Source trips is Bilaspur.
24. The most trips State and Place source wise are Haryana and Bilaspur.
25. The most trips State and City source wise are Haryana and Bilaspur.
26. The most trips State and Place destination wise are Haryana and Bilaspur.
27. The most trips State and City destination wise are Karnataka and Bengaluru.
28. The most trips are between Cities bangalore, bengaluru and hyderabad. Most trips are within city trips.
29. The most trips are between States Maharashtra, Karnataka and Tamil Nadu. Most trips are within state trips.
30. The most trips are between Central, Bilaspur, KGAirport and Nelmngla. Most trips are within place trips.
31. Almost all of the data is from September.
32. Most of the trips start on Wednesday or Saturday.
33. In terms of Source state, Mizoram state has the highest difference in actual time and osrm time. While Dadra and nagar haveli have the lowest.
34. In terms of Destination state, Mizoram state has the highest difference in actual time and osrm time. While Dadra and nagar haveli have the lowest.
35. The Data in the columns is not gaussian so we scale it using a min-max scaler.

**Recommendations**



1. As the carting segment is most used the company can develop its infra for this route type. Also it gives faster delivery as compared to FTL.
2. Most of the products were delivered on Wednesday and Saturday, so it is preferable for customers to get products during weekdays rather than weekends.
3. There is significant difference in actual time and osrm time so it indicates that the deliveries are not optimized and most of them are delivered past the deadline.
4. Also there is a significant difference between actual time and segment actual time so it gives a hint of carelessness in the logistics chain and management.
5. There is also a significant difference between osrm distance and segment osrm distance denoting that the distance calculation engine is buggy. The company can try to integrate various newer engines like google maps which takes into account the traffic condition and calculates the best route.
6. The company can increase its working capacity during the middle of the month.
7. For the States, Cities and places with most destination or source  trips the company can increase their warehouses. For cities like bengaluru and gurgaon setting up multiple chain houses is profitable.
8. As most of the trips are between cities/states it will be easier to deliver them faster and quicker if the company has various warehouses within cities/states.
9. The company to needs to develop its logistics for states like mizoram and himachal pradesh where osrm distance/time is very different from actual distance/time.
10. The company is mainly focusing on metropolitan states/cities by neglecting less developed states. The company also need a well developed infra for these states also.