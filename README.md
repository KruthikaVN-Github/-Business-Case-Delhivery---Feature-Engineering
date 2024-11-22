# Delhivery - Feature Engineering
-- Objective
The purpose of this analysis is to explore the data, uncover patterns, and derive actionable insights to improve the operational efficiency of Delhivery's logistics and delivery processes. The analysis aims to contribute to the development of a more robust and intelligent system for managing logistics data, optimizing routes, and reducing delivery times.

# Dataset Overview
The data in this repository is used to build intelligence that aids Delhivery's data team in optimizing their operations. The dataset includes various columns that represent key metrics related to trips, routes, and delivery efficiency. Below is a description of the key columns in the dataset:

# Columns
data: Indicates whether the data is for testing or training purposes.
trip_creation_time: Timestamp when the trip was created.
route_schedule_uuid: Unique identifier for a particular route schedule.
route_type: Type of transportation (e.g., FTL, Carting).
FTL: Full Truck Load shipments. These shipments reach the destination sooner, as the truck makes no other pickups or drop-offs along the way.
Carting: Refers to the handling system involving small vehicles or carts.
trip_uuid: Unique identifier for a particular trip (can include different source and destination centers).
source_center: Source ID of the trip origin.
source_name: Name of the trip origin.
destination_center: Destination ID of the trip.
destination_name: Name of the destination center.
od_start_time: Timestamp when the trip starts.
od_end_time: Timestamp when the trip ends.
start_scan_to_end_scan: Time taken to deliver from source to destination.
is_cutoff: Unknown field.
cutoff_factor: Unknown field.
cutoff_timestamp: Unknown field.
actual_distance_to_destination: Actual distance (in km) between the source and destination warehouse.
actual_time: Actual time taken to complete the delivery (cumulative).
osrm_time: Time calculated using OSRM (Open Source Routing Machine) engine, which computes the shortest path and estimates delivery time, considering traffic and road conditions.
osrm_distance: Distance computed using OSRM engine, accounting for traffic and road conditions.
factor: Unknown field.
segment_actual_time: Time taken by a subset of the package delivery.
segment_osrm_time: Time calculated for a subset of the package delivery using OSRM.
segment_osrm_distance: Distance covered by a subset of the package delivery using OSRM.
segment_factor: Unknown field.
