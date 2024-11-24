# 🚚 Delhivery - Feature Engineering

## 📋 Overview
This project focuses on **Feature Engineering** for logistics data from Delhivery, one of the leading supply chain companies in India. The dataset provides insights into transportation logistics, including route planning, delivery times, and distance calculations. The project leverages advanced data analysis and engineering techniques to extract meaningful features and improve operational efficiency.

---

## 🎯 Objectives
1. Analyze and preprocess the logistics dataset for **training and testing purposes**.
2. Engineer new features to enhance the predictive power of machine learning models.
3. Identify key factors influencing delivery performance, such as route type, actual distance, and delivery time.
4. Provide actionable insights for optimizing **last-mile delivery logistics**.

---

## 📂 Dataset Description
The dataset contains detailed information about transportation logistics, including timestamps, route details, and distance metrics. Below is a description of the key columns:

| **Column Name**             | **Description**                                                                 |
|-----------------------------|---------------------------------------------------------------------------------|
| `data`                      | Indicates whether the data is for testing or training purposes.                |
| `trip_creation_time`        | Timestamp when the trip was created.                                           |
| `route_schedule_uuid`       | Unique identifier for a particular route schedule.                             |
| `route_type`                | Type of transportation (e.g., FTL, Carting).                                   |
| `FTL`                       | Full Truck Load shipments, which are faster as there are no additional stops.  |
| `Carting`                   | Small vehicle shipments involving multiple pickups/drop-offs.                  |
| `trip_uuid`                 | Unique identifier for a particular trip.                                       |
| `source_center`             | Source ID of the trip origin.                                                  |
| `source_name`               | Name of the trip origin.                                                       |
| `destination_center`        | Destination ID of the trip.                                                    |
| `destination_name`          | Name of the destination center.                                                |
| `od_start_time`             | Timestamp when the trip starts.                                                |
| `od_end_time`               | Timestamp when the trip ends.                                                  |
| `start_scan_to_end_scan`    | Time taken to deliver from source to destination.                               |
| `is_cutoff`                 | Unknown field.                                                                 |
| `cutoff_factor`             | Unknown field.                                                                 |
| `cutoff_timestamp`          | Unknown field.                                                                 |
| `actual_distance_to_destination` | Actual distance (in km) between the source and destination warehouse.     |
| `actual_time`               | Actual time taken to complete the delivery (cumulative).                       |
| `osrm_time`                 | Time calculated using the OSRM (Open Source Routing Machine) engine.           |
| `osrm_distance`             | Distance calculated using the OSRM engine.                                     |
| `factor`                    | Unknown field.                                                                 |
| `segment_actual_time`       | Time taken for a subset of the package delivery.                               |
| `segment_osrm_time`         | OSRM-calculated time for a subset of the delivery.                             |
| `segment_osrm_distance`     | Distance covered for a subset of the delivery (calculated by OSRM).            |
| `segment_factor`            | Unknown field.                                                                 |

---

## 🔧 Key Skills and Tools
This project demonstrates proficiency in:
- **Programming Languages**: Python  
- **Libraries**:
  - **Pandas**: For data preprocessing, cleaning, and manipulation.
  - **NumPy**: For numerical calculations.
  - **Matplotlib & Seaborn**: For data visualization.
  - **Techniques**:
  - Exploratory Data Analysis (EDA)
  - Feature Engineering
  - Time-Series Analysis
  - Geospatial Data Analysis
  - Optimization of Logistic Routes

---

## 📊 Steps Performed
1. **Data Cleaning**:
   - Handled missing values and corrected inconsistencies in fields such as `source_name` and `destination_name`.
   - Converted timestamps into usable date-time formats for time-based analysis.

2. **Exploratory Data Analysis (EDA)**:
   - Analyzed route types (`FTL`, `Carting`) and their impact on delivery time and distance.
   - Investigated correlations between `osrm_time`, `actual_time`, and `segment_actual_time`.

3. **Feature Engineering**:
   - Derived new features such as:
     - **Delivery Efficiency**: Ratio of `actual_time` to `osrm_time`.
     - **Deviation Factor**: Difference between `actual_distance_to_destination` and `osrm_distance`.
     - **Trip Duration**: Derived from `od_start_time` and `od_end_time`.
   - Binned continuous variables (e.g., `actual_distance_to_destination`) for categorical analysis.

4. **Insights Generation**:
   - Identified key factors contributing to delayed deliveries.
   - Highlighted route optimization opportunities based on `segment_osrm_time` and `segment_actual_time`.

---

## 📈 Key Insights
- **Route Type**:
  - **FTL** shipments consistently have shorter delivery times compared to **Carting**.
  - **Carting** shipments experience delays due to multiple stops and higher `segment_actual_time`.
- **Distance and Time**:
  - Discrepancies between `osrm_time` and `actual_time` highlight potential inefficiencies in routing or traffic estimation.
- **Geographical Patterns**:
  - Specific source-destination pairs have consistently higher deviations in delivery times, suggesting optimization opportunities.

---


