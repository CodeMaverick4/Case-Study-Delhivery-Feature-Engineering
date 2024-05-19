# From Raw Data to Predictive Models: A Delhivery Case Study 🚚📊

This repository contains a comprehensive analysis of Delhivery's dataset to derive valuable insights and build forecasting models. Delhivery, the largest and fastest-growing fully integrated player in India by revenue in Fiscal 2021, aims to revolutionize commerce through top-notch infrastructure, logistics operations, and cutting-edge engineering and technology capabilities.

## About Delhivery 

Delhivery is on a mission to develop the operating system for commerce, leveraging world-class infrastructure, logistics operations, and cutting-edge technology. The Data team plays a crucial role by harnessing data to enhance the quality, efficiency, and profitability of Delhivery's operations.

## Objective 🎯

The primary objective of this analysis is to understand and process data from Delhivery's data engineering pipelines. Specifically, we aim to:

- Clean, sanitize, and manipulate data to extract useful features from raw fields.
- Make sense of the raw data to aid the data science team in building forecasting models.

## Column Profiling 🔍

The dataset comprises several columns with specific information related to Delhivery's operations. Key columns include:

- `data`: Indicates whether the data is testing or training data.
- `trip_creation_time`: Timestamp of trip creation.
- `route_schedule_uuid`: Unique ID for a particular route schedule.
- `route_type`: Transportation type (e.g., FTL, Carting).
- `trip_uuid`: Unique ID for a particular trip.
- `source_center`, `source_name`: Source ID and name of trip origin.
- `destination_center`, `destination_name`: Destination ID and name.
- `od_start_time`, `od_end_time`: Trip start and end times.
- `start_scan_to_end_scan`: Time taken to deliver from source to destination.
- `actual_distance_to_destination`: Distance in Kms between source and destination.
- `actual_time`, `osrm_time`: Actual time and OSRM time taken for delivery.
- `segment_actual_time`, `segment_osrm_time`: Segment time for package delivery.
- `segment_osrm_distance`: OSRM distance covered by package delivery.

## Concept Used 💡

The analysis involves various data processing and analysis techniques, including:

- Feature Creation
- Relationship between Features
- Column Normalization / Column Standardization
- Handling Categorical Values
- Missing Values Treatment / Outlier Detection and Treatment
- One-Hot Encoding
- Normalization / Standardization of Numerical Features

## Approach 🚀

1. **Basic Data Cleaning and Exploration:**
   - Handle missing values in the data.
   - Analyze the structure of the data.
   - Merge rows based on trip details and aggregate relevant information.
   - Build features from destination name, source name, and trip creation time.

2. **In-depth Analysis and Feature Engineering:**
   - Calculate the time taken between `od_start_time` and `od_end_time`.
   - Compare different time metrics.
   - Conduct hypothesis testing and visual analysis.
   - Identify and handle outliers.
   - Perform one-hot encoding of categorical variables.
   - Normalize/Standardize numerical features

#**Business Insights & Recommendations**

##**Insights**
- Catering orders comprise approximately 51% of total orders, while FTL orders make up the remaining 49%. This indicates a
slightly higher demand for smaller shipments handled by catering services.
- The data suggests a significant volume of deliveries to states like Maharashtra and Karnataka, as they have the highest number
of unique trip_uuids. Conversely, states like Himachal Pradesh, Chandigarh, and Goa show lower delivery volumes.
- Evening and night-time periods experience a surge in trip planning and logistics activities, possibly due to preparations for nextday deliveries, optimization of nighttime transportation routes, and customer preferences for evening deliveries.
- Mumbai emerges as the top city for Delhivery services in Maharashtra, indicating its importance as a major hub for sending and
receiving packages. Similarly, Bengaluru leads in Delhivery services in Karnataka, reflecting its significance as a bustling city with
high delivery demand.
- The average distance traveled from source to destination is approximately 93 kilometers, highlighting the typical distance
covered by deliveries.
- On average, trips take close to 6 hours to complete, indicating the typical duration of delivery operations.
- The hypothesis testing conducted on actual time, distance, and segmented distance and time compared to estimated time,
distance, and segmented distance and time resulted in rejecting the null hypothesis. This suggests that there are significant
differences between the actual and estimated values, indicating potential areas for further investigation and optimization in
delivery operations. This implies a need to improve the open-source routing engine to enhance accuracy and efficiency in route
planning and delivery estimations.

#**Recommendation**
- More customers prefer smaller shipments handled by catering services, like carts, than larger shipments needing dedicated
transportation. So, businesses can focus on catering services to cater to this higher demand.
- Maharashtra, Karnataka have the highest delivery volumes, so businesses can focus on expanding their delivery services in
these states and cities to attract more customers.
- Evening and night-time periods experience a surge in trip planning and logistics activities, so businesses can optimize their
delivery routes and schedules during these hours to improve efficiency and reduce delivery times.
- The average distance of a trip is close to 93 KM, and the average time taken by a trip is close to 6 hours. This information can
help businesses optimize their delivery routes and estimate delivery times more accurately.
- Businesses can invest in data analytics to study and analyze their delivery data to identify trends, patterns, and opportunities for
improvement, and make data-driven business decisions
- Business should switch to other better open source routing engine which give more accurate preditons about time and distance


#**Thank you for visiting!**
