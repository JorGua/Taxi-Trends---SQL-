# Taxi Trends - SQL

The task was to find patterns in the database with information on taxi rides in Chicago to understand passenger preferences and the impact of external factors on rides. To begin the analysis, first, we counted the number of taxi rides for each company on November 15-16, 2017, to find the top taxi companies (Flash Cab and Taxi Affiliation Services). Additionally, we identified the number of rides in November 2017 for Flash Cab and Taxi Affiliation Services.

Following this, we determined how the duration of rides from the Loop to O'Hare International Airport varied on rainy Saturdays compared to other days. We retrieved the neighborhood IDs for O'Hare and the Loop and categorized hourly weather records as "Bad" (rain/storm) or "Good" (other) using the CASE operator. Finally, we retrieved rides that started in the Loop and ended at O'Hare on Saturdays, obtained the weather conditions and durations for these rides, and excluded rides with missing weather data.

## Description of the data

### Neighborhoods table: 
-	name: name of the neighborhood
-	neighborhood_id: neighborhood code
### Cabs table: 
-	cab_id: vehicle code
-	vehicle_id: the vehicle's technical ID
-	company_name: the company that owns the vehicle
### Trips table: 
-	trip_id: ride code
-	cab_id: code of the vehicle operating the ride
-	start_ts: date and time of the beginning of the ride (time rounded to the hour)
-	end_ts: date and time of the end of the ride (time rounded to the hour)
-	duration_seconds: ride duration in seconds
-	distance_miles: ride distance in miles
-	pickup_location_id: pickup neighborhood code
-	dropoff_location_id: dropoff neighborhood code
### Weather_records table: 
-	record_id: weather record code
-	ts: record date and time (time rounded to the hour)
-	temperature: temperature when the record was taken

## Table Scheme

![Screenshot 2024-07-16 141802](https://github.com/user-attachments/assets/fc53b6fe-9494-4f2b-b969-cbba48c142b2)

