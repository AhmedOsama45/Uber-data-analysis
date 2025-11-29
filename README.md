# Uber Ride Data Analysis Project (NCR Region)

**Team Analatica**
* Ahmed Osama Mohamed Mobarez
* Fawzy Mohamed Ahmed Shams
* Anton Samy Tawfeek
* Ahmed Hessien Ahmed
* Essam Mohamed Ahmed
* Hassan Ashraf

---

[cite_start]This repository contains the data analysis and visualization project for Uber ride data in the NCR Region (Jan 2024 – Dec 2024)[cite: 3, 20]. The project involves cleaning and processing a raw dataset to extract key performance indicators (KPIs) and build an interactive dashboard using Power BI.

## Project Objective

The primary goal of this project is to analyze Uber ride data to uncover booking patterns and gain insights into operational performance. [cite_start]This analysis supports data-driven decision-making aimed at optimizing services, improving customer experience, and understanding driver behavior[cite: 17].

## Repository Contents

* [cite_start]**`Blue and White Modern Data Analysis Presentation.pptx`**: The final presentation deck summarizing key insights, KPIs, and strategic recommendations[cite: 1, 71].
* [cite_start]**`enhanced bi.pbix`**: The Power BI desktop file containing the final interactive dashboard and data model[cite: 12].
* **`Uber-data-analysis.ipynb`**: A Jupyter Notebook containing the Python code (using pandas and NumPy) for data cleaning, transformation, and initial analysis.
* **`Uber data analysis Documentation.pdf`**: A document outlining the project proposal, plan, data dictionary, and dashboard design.
* **`README.md`**: This file, providing an overview of the project.

## Data Overview

[cite_start]The dataset consists of approximately 150,000 ride records [cite: 21] with the following attributes:

* **Booking ID, Customer ID, Driver ID**: Unique identifiers.
* **Date & Time**: Timestamp of the booking.
* **Booking Status**: Final status (e.g., Completed, Cancelled by Customer, Cancelled by Driver, Incomplete).
* **Vehicle Type**: Auto, Bike, Go Sedan, etc.
* **Pickup & Drop Location**: Start and end points of the ride.
* **Avg VTAT & CTAT**: Vehicle/Customer Turn Around Time (wait times).
* **Booking Value**: Fare amount.
* **Ride Distance**: Distance in kilometers.
* **Driver & Customer Ratings**: Mutual ratings (1-5).
* **Payment Method**: UPI, Debit Card, Cash.
* **Cancellation Reasons**: Specific reasons provided by drivers or customers.

## Data Cleaning and Preparation

[cite_start]The `Uber-data-analysis.ipynb` notebook details the data cleaning process, which includes[cite: 25, 26, 27]:

* **Handling Missing Values**:
    * Imputing `Avg VTAT`, `Avg CTAT`, `Booking Value`, and `Ride Distance` using group-based means (e.g., by location, vehicle type).
    * Filling `NaN` values in cancellation columns with `0` or appropriate labels.
* **Data Correction**:
    * Validating data to remove logical inconsistencies and ensure high data integrity.

## Key Performance Indicators (KPIs)

Based on the analysis of ~150,000 bookings:

* [cite_start]**Total Booking Value**: $76 Million [cite: 32]
* [cite_start]**Completion Rate**: 62.01% [cite: 34]
* [cite_start]**Cancellation Rate**: 25% [cite: 35]
    * [cite_start]*Driver Cancellations*: 72% of all cancellations (Primary reasons: Personal/Car issues) [cite: 47, 51, 52]
    * [cite_start]*Customer Cancellations*: 28% of all cancellations (Primary reasons: Wrong Address, Change of Plans) [cite: 48, 55, 56]
* [cite_start]**Incomplete Ride Rate**: ~13% [cite: 36]

---

* [cite_start]**Average Booking Value**: $508 [cite: 58]
* [cite_start]**Average Ride Distance**: 24.66 km [cite: 59]
* [cite_start]**Wait Times (CTAT)**: Average 29.15 minutes (a key driver of cancellations) [cite: 85]
* [cite_start]**Payment Method**: UPI dominates with 62.6% share [cite: 61]

## Dashboard & Visualization

The `enhanced bi.pbix` file contains an interactive dashboard designed to explore this data. [cite_start]Key features include[cite: 12, 13, 14, 15, 16]:

* **Executive Overview**: Monthly trends (Peak in July) and high-level KPIs.
* **Vehicle Dashboard**: Fleet mix analysis (Auto is the highest revenue generator).
* **Cancellation Dashboard**: Deep dive into reasons for driver vs. customer cancellations.
* **Revenue & Distance**: Financial performance and trip analysis.
* **Search Feature**: A granular tracking tool to search any **Booking ID** and view specific status, revenue, and ratings.

## Strategic Recommendations

[cite_start]Based on the findings, the team proposes the following strategies[cite: 71, 72, 74, 76, 78]:

1.  **Reduce Cancellations**: Implement penalties for unjustified driver cancellations and improve pickup location accuracy.
2.  **Improve Wait Times**: Incentivize drivers in high-demand locations to reduce Customer Turn Around Time (CTAT).
3.  **Fleet Optimization**: Promote "Premier" and "Uber XL" tiers to diversify revenue beyond "Auto".
4.  **Digital Payment Expansion**: Build on the dominance of UPI through wallet partnerships and digital incentives.

---
*This README was generated based on the provided project files and presentation.*
