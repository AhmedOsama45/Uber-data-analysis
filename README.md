# Uber Ride Data Analysis Project

This repository contains the data analysis and visualization project for Uber ride data. The project involves cleaning and processing a raw dataset to extract key performance indicators (KPIs) and build an interactive dashboard using Power BI.

## Project Objective

The primary goal of this project is to analyze Uber ride data to uncover booking patterns and gain insights into operational performance. This analysis supports data-driven decision-making aimed at optimizing services, improving customer experience, and understanding driver behavior.

## Repository Contents

* **`Uber-data-analysis.ipynb`**: A Jupyter Notebook containing the Python code (using pandas and NumPy) for data cleaning, transformation, and initial analysis.
* **`Uber data analysis Documentation.pdf`**: A document outlining the project proposal, plan, data dictionary, and dashboard design.
* **`enhanced bi.pbix`**: The Power BI desktop file containing the final interactive dashboard and data model.
* **`README.md`**: This file, providing an overview of the project.

## Data Overview

The dataset consists of 150,000 ride records with the following attributes:

* **Booking ID**: Unique identifier for each ride booking.
* **Customer ID**: Unique identifier for each customer.
* **Driver ID**: Unique identifier for each driver.
* **Date**: Date the booking was made.
* **Time**: Time the booking was made.
* **Booking Status**: The final status of the ride (e.g., Completed, Cancelled by Customer, Cancelled by Driver, Incomplete, No Driver Found).
* **Vehicle Type**: Type of vehicle used (e.g., Auto, Bike, Go Sedan).
* **Pickup Location**: Starting point of the ride.
* **Drop Location**: Destination of the ride.
* **Avg VTAT**: Vehicle Turn Around Time (in minutes).
* **Avg CTAT**: Customer Turn Around Time (in minutes).
* **Booking Value**: The fare for the ride.
* **Ride Distance**: The distance of the ride in kilometers.
* **Driver Ratings**: Rating given by the customer to the driver (1-5).
* **Customer Rating**: Rating given by the driver to the customer (1-5).
* **Payment Method**: Mode of payment (e.g., UPI, Debit Card, Cash).
* **Reason for cancelling by Customer**: Reason provided by the customer for cancellation.
* **Driver Cancellation Reason**: Reason provided by the driver for cancellation.
* **Incomplete Rides Reason**: Reason provided for incomplete rides.

## Data Cleaning and Preparation

The `Uber-data-analysis.ipynb` notebook details the data cleaning process, which includes:

* **Handling Missing Values**:
    * Imputing `Avg VTAT`, `Avg CTAT`, `Booking Value`, and `Ride Distance` using group-based means (e.g., by location, vehicle type) and falling back to the overall mean where necessary.
    * Filling `NaN` values in cancellation and incomplete ride columns with `0` (for counts) or appropriate string labels (e.g., "Not Cancelled").
* **Data Correction**:
    * Setting `Driver Ratings` and `Customer Rating` to `NaN` for all non-completed rides (cancelled or incomplete) to avoid skewing rating averages. These `NaN`s are then filled with `0` to represent "Not Applicable".

## Key Performance Indicators (KPIs)

Based on the analysis of 150,000 bookings:

* **Completion Rate**: 62.0% (93,000 rides)
* **Driver Cancellation Rate**: 18.0% (27,000 rides)
* **Customer Cancellation Rate**: 7.0% (10,500 rides)
* **Incomplete Ride Rate**: 6.0% (9,000 rides)
* **No Driver Found Rate**: 7.0% (10,500 rides)

---

* **Average Booking Value**: ₹507.76
* **Average Ride Distance**: 24.66 km
* **Average Vehicle Turn Around Time (VTAT)**: 8.46 minutes
* **Average Customer Turn Around Time (CTAT)**: 29.15 minutes

## Dashboard & Visualization

The `enhanced bi.pbix` file contains an interactive dashboard designed to explore this data. Key features include:

* **Executive Overview**: A high-level look at total rides, revenue, completion rates, and average ratings.
* **Booking Analysis**: Detailed breakdown of ride statuses (completed, cancelled, etc.) by vehicle type and time.
* **Cancellation Analysis**: Visualizations exploring the primary reasons for both driver and customer cancellations.
* **Performance Metrics**: Analysis of wait times, ride distance, and revenue by payment method.
* **Geographic Insights**: Maps showing ride volume and revenue by pickup and drop-off locations.

---
