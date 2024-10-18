## IA626_Nipun_NYC_Taxi-_trips_Part-1

### Dataset : trip_data_10.csv

### Questions 

### 1. What datetime range does your data cover?  How many rows are there total?
  
| Attribute                     | Value                                         |
|-------------------------------|-----------------------------------------------|
| `Pickup Datetime Range`       | 2013-10-01 00:00:00 to 2013-10-31 23:59:59     |
|` Dropoff Datetime Range`      | 2013-10-01 00:00:00 to 2013-11-01 03:17:34     |
|` Row count including header`  | 15004556                                      |

                         
### 2. What are the field names?  Give descriptions for each field.
  
| Field                | Description                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------|
| `medallion`          | A unique identifier for each taxi cab.                                                              |
| `hack_license`       | A unique identifier for the taxi driver's license.                                                  |
| `vendor_id`          | Code indicating the provider of the taxi service.                                                   |
| `rate_code`          | The rate code used for the trip, indicating the type of fare charged.                               |
| `store_and_fwd_flag` | Indicates whether the trip data was stored in the vehicle's memory before being sent to the server. |
| `pickup_datetime`    | The date and time when the passenger(s) were picked up.                                             |
| `dropoff_datetime`   | The date and time when the passenger(s) were dropped off.                                           |
| `passenger_count`    | The number of passengers in the trip.                                                               |
| `trip_time_in_secs`  | The total duration of the trip in seconds.                                                          |
| `trip_distance`      | The distance of the trip in miles or kilometers.                                                    |
| `pickup_longitude`   | The longitude coordinate of the location where the passenger was picked up.                         |
| `pickup_latitude`    | The latitude coordinate of the location where the passenger was picked up.                          |
| `dropoff_longitude`  | The longitude coordinate of the location where the passenger was dropped off.                       |
| `dropoff_latitude`   | The latitude coordinate of the location where the passenger was dropped off.                        |


### 3. Give some sample data for each field.

| Field Names        | Sample Data                      |
|--------------------|----------------------------------|
| `medallion`        | 740BD5BE61840BE4FE3905CC3EBE3E7E |
| `hack_license`     | E48B185060FB0FF49BE6DA43E69E624B |
| `vendor_id`        | CMT                              |
| `rate_code`        | 1                                |
| `store_and_fwd_flag`| N                               |
| `pickup_datetime`  | 2013-10-01 12:44:29              |
| `dropoff_datetime` | 2013-10-01 12:53:26              |
| `passenger_count`  | 1                                |
| `trip_time_in_secs`| 536                              |
| `trip_distance`    | 1.20                             |
| `pickup_longitude` | -73.974319                       |
| `pickup_latitude`  | 40.741859                        |
| `dropoff_longitude`| -73.99115                        |
| `dropoff_latitude` | 40.742424                        |


### 4. What MySQL data types / len would you need to store each of the fields?

| Column Name        | Data Type        |
|--------------------|------------------|
| `medallion`        | VARCHAR(32)      |
| `hack_license`     | VARCHAR(32)      |
| `vendor_id`        | VARCHAR(3)       |
| `rate_code`        | INT           |
| `store_and_fwd_flag`| BOOLEAN         |
| `pickup_datetime`  | DATETIME         |
| `dropoff_datetime` | DATETIME         |
| `passenger_count`  | INT           |
| `trip_time_in_secs`| INT          |
| `trip_distance`    | DECIMAL(5,2)     |
| `pickup_longitude` | DECIMAL(10,6)     |
| `pickup_latitude`  | DECIMAL(10,6)     |
| `dropoff_longitude`| DECIMAL(10,6)     |
| `dropoff_latitude` | DECIMAL(10,6)     |


### 5. What is the geographic range of your data (min/max - X/Y)? Plot this (approximately on a map)

| Attribute       | Min Value   | Max Value   |
|-----------------|-------------|-------------|
| Longitude Range | -74.0312    | -73.9263    |
| Latitude Range  | 40.6843     | 40.8182     |


#### Map Plot 
![Map](https://github.com/user-attachments/assets/743cc4af-0434-40f8-b17c-6f47db6b5cfa)


### 6. What is the average overall computed trip distance? (You should use Haversine Distance). Draw a histogram of the trip distances binned anyway you see fit.

The average trip distance is: 10.252114787644716 miles
#### Histogram
![histogram](https://github.com/user-attachments/assets/6d25338e-2bb8-4451-84b3-d3f9a0dfc58b)



### 7. What are the distinct values for each field? (If applicable)

| Attribute               | Values                                                          |
|-------------------------|-----------------------------------------------------------------|
| `Vendor IDs`              | ['VTS', 'CMT']                                                  |
| `Rate Codes`              | ['210', '0', '7', '8', '2', '5', '3', '9', '28', '6', '1', '4'] |
|`Store and Forward Flags` | ['', 'N', 'Y']                                                  |
| `Passenger Counts`        | ['0', '7', '2', '5', '3', '9', '6', '1', '4']                   |


### 8. For other numeric types besides lat and lon, what are the min and max values?

| Attribute         | Min Value | Max Value |
|-------------------|-----------|-----------|
| `Rate Code`       | 0         | 9         |
| `Passenger Count` | 0         | 9         |
| `Trip Time (secs)` | 0         | 9999      |
| `Trip Distance`   | 0         | 99.2      |

### 9. Create a chart which shows the average number of passengers each hour of the day. (X axis should have 24 hours)
![Q9](https://github.com/user-attachments/assets/c2fb0bdb-8b0a-40b0-8815-e02170e2bf03)

### 10. Create a new CSV file which has only one out of every thousand rows.
New created file can be generated by running the code

### 11.	Repeat step 9 with the reduced dataset and compare the two charts.
![Q11](https://github.com/user-attachments/assets/aaf0f161-3c13-4b3a-bb5c-1655f9fc5d59)

- Chart comparison shows that there is a low demand for taxi rides between 6th and 7th hour of the day. This trend is seen in original dataset as well as the reduced dataset. 





  
