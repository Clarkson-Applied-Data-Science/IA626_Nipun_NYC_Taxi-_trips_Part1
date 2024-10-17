## IA626_Nipun_NYC_Taxi-_trips_Part-1

### Dataset : trip_data_10.csv

### Questions 
- What datetime range does your data cover?  How many rows are there total?
  
| Attribute                     | Value                                         |
|-------------------------------|-----------------------------------------------|
| `Pickup Datetime Range`       | 2013-10-01 00:00:00 - 2013-10-31 23:59:59     |
|` Dropoff Datetime Range`      | 2013-10-01 00:00:00 - 2013-11-01 03:17:34     |
|` Row count including header`  | 15004557                                      |

                         
- What are the field names?  Give descriptions for each field.
  
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


- Give some sample data for each field.

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


- What MySQL data types / len would you need to store each of the fields?

| Column Name        | Data Type        |
|--------------------|------------------|
| `medallion`        | VARCHAR(32)      |
| `hack_license`     | VARCHAR(32)      |
| `vendor_id`        | VARCHAR(3)       |
| `rate_code`        | INT(3)           |
| `store_and_fwd_flag`| BOOLEAN          |
| `pickup_datetime`  | DATETIME         |
| `dropoff_datetime` | DATETIME         |
| `passenger_count`  | INT(3)           |
| `trip_time_in_secs`| INT(10)          |
| `trip_distance`    | DECIMAL(4,2)     |
| `pickup_longitude` | DECIMAL(3,6)     |
| `pickup_latitude`  | DECIMAL(3,6)     |
| `dropoff_longitude`| DECIMAL(3,6)     |
| `dropoff_latitude` | DECIMAL(3,6)     |

  
  

  
