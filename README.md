## IA626_Nipun_NYC_Taxi-_trips_Part-1

### Dataset : trip_data_10.csv

### Questions 
- What datetime range does your data cover?  How many rows are there total?
  
| Attribute                     | Value                                         |
|-------------------------------|-----------------------------------------------|
| `Pickup Datetime Range`       | 2013-10-01 00:00:00 to 2013-10-31 23:59:59     |
|` Dropoff Datetime Range`      | 2013-10-01 00:00:00 to 2013-11-01 03:17:34     |
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
| `store_and_fwd_flag`| BOOLEAN         |
| `pickup_datetime`  | DATETIME         |
| `dropoff_datetime` | DATETIME         |
| `passenger_count`  | INT(3)           |
| `trip_time_in_secs`| INT(10)          |
| `trip_distance`    | DECIMAL(4,2)     |
| `pickup_longitude` | DECIMAL(5,6)     |
| `pickup_latitude`  | DECIMAL(5,6)     |
| `dropoff_longitude`| DECIMAL(5,6)     |
| `dropoff_latitude` | DECIMAL(5,6)     |


- What is the geographic range of your data (min/max - X/Y)? Plot this (approximately on a map)

| Attribute                | Range                   |
|--------------------------|-------------------------|
| `Pickup Longitude Range`    | -74.258698 to -73.70034  |
| `Pickup Latitude Range`     | 40.485001 to 40.917484   |
| `Dropoff Longitude Range`  | -74.258698 to -73.700272 |
| `Dropoff Latitude Range`    | 40.481312 to 40.917568   |

#### Plot 
![Capture](https://github.com/user-attachments/assets/87286f84-bfdf-4fd2-aa2d-8756ae5aff20)


- What is the average overall computed trip distance? (You should use Haversine Distance). Draw a histogram of the trip distances binned anyway you see fit.



- What are the distinct values for each field? (If applicable)

| Attribute               | Values                                                                                                                                                                               |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Medallions`              | ['115166F8B584AADB44EAB0B0E8240F8B', 'E6E5919C2782FCC4D9BC84E48A84C64B', 'E3292CAFA701D5DD70AD44148050ED9A', '723F4EC1E70E69A884423C87795E74D2', 'A910CF5A84FFE5F10B8CCBC06CC5F944'] |
| `Hack Licenses`           | ['6CE9D8A210B4E79D629F37C17B653F1A', '4B47F53D9856A828C6E5CA9B02DEFE5F', 'FBCA24C1B0ADB56EE291F4C419860070', 'A7725619DC0B5CDAD027F19ABB7FECA0', 'D362B392C8E55DF20A73F814A63DE173'] |
| `Vendor IDs`              | ['VTS', 'CMT']                                                                                                                                                                       |
| `Rate Codes`              | ['2', '210', '5', '6', '3']                                                                                                                                                          |
| `Store and Forward Flags` | ['', 'Y', 'N']                                                                                                                                                                       |
| `Pickup Datetimes`        | ['2013-10-07 13:20:29', '2013-10-03 22:18:53', '2013-10-21 08:59:07', '2013-10-18 21:02:50', '2013-10-19 19:17:42']                                                                  |
| `Dropoff Datetimes`       | ['2013-10-07 13:20:29', '2013-10-03 22:18:53', '2013-10-21 08:59:07', '2013-10-18 21:02:50', '2013-10-19 19:17:42']                                                                  |
| `Passenger Counts`        | ['2', '5', '6', '3', '0']                                                                                                                                                            |
| `Trip Times (in seconds)` | ['5790', '8033', '2884', '6120', '1863']                                                                                                                                             |
| `Trip Distances`          | ['.56', '8.26', '17.00', '5.91', '16.57']                                                                                                                                            |
| `Pickup Longitudes`       | ['-73.765411', '-73.904625', '-73.962646', '-73.856339', '-73.797714']                                                                                                               |
| `Pickup Latitudes`        | ['40.690987', '40.730583', '40.690014', '40.699039', '40.733723']                                                                                                                    |
| `Dropoff Longitudes`      | ['', '-73.765411', '-73.688354', '-74.086716', '-73.702919']                                                                                                                         |
| `Dropoff Latitudes`       | ['', '40.690987', '40.690014', '40.699039', '40.733723']                                                                                                                             |


  



  
