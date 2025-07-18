# Project Background
 In the competitive and dynamic hospitality industry, hotels and resorts frequently encounter
 revenue leakages, underutilized capacity, and fluctuating profitability. These challenges arise
 due to factors such as inefficient pricing strategies, inconsistent demand across weekdays and
 weekends, underperformance of specific room types or service offerings, and lack of actionable
 insights from available customer and booking data.
 
 This project, conducted under the **Consulting & Analytics Club, IIT Guwahati**, aims to
 address these issues by leveraging historical booking data from a leading hotel chain to
 uncover patterns and inefficiencies. The objective is to design an end-to-end analytical
 framework that identifies root causes of revenue leakage, supports informed decision-making
 through actionable insights, and quantifies the business impact of strategic recommendations.

 **AtliQ Grands** (*a hypothetical hotel enterprise group*) owns multiple five-star hotels across India. They have been in the hospitality industry for the past 20 years. Due to strategic moves from other competitors and ineffective decision-making in management, AtliQ Grands are losing their market share and revenue in the luxury/business hotels category. As a strategic move, the managing director of AtliQ Grands wanted to incorporate “Business and Data Intelligence” to regain their market share and revenue.

 Insights and recommendations are provided on the following key areas:

 - **Revenue Trend Analysis:**  Evaluation of historical revenue patterns, both by property name and by region, focusing on RevPar and Average Daily Revenue (ADR).
 - **Bookings Analysis:**  Distribution of bookings across room class, platform, and day type, understanding the reason behind revenue leakage.
 - **Generated vs Realized:**  An evaluation of actual revenue realized by the properties and how deviated it is from the revenue generated.
 - **What‑If ROI Simulator:**  Models how modest increases in premium bundling, cancellation mitigation, or direct‑booking shifts can recapture millions and improve ROI up to ~2%.

An interactive Power BI dashboard used to analyze and explore the above-mentioned insights can be found here. [link](https://app.powerbi.com/groups/me/reports/0be65715-f1d4-4d39-bb05-89f79e85f4bb/1781d5352c50911cbc29?experience=power-bi)


# Data Structure & Initial Checks
The company's main database structure, as seen below, consists of four tables:
- ***dim_data:***  It is the date table (consisting of 92 rows).
- ***dim_hotels:***  It is the property table summarizing different properties, categories for each property and cities (consisting of 25 rows).
- ***dim_rooms:***  It is the room class table (such as Standard, Presidential, etc.) (consisting of 4 rows).
- ***fact_aggregated_bookings:***  Displaying the check-in date for each room and number of successful bookings per check-in date (consisting of 9200 rows).
- ***fact_bookings:***  The most crucial table in the whole database, containing all details related to bookings, such as booking data, check_in date, check_out date, booking_status, revenue generated, etc.
- ***Key Measures:***  Containing all the calculated measures used in the project.
  
![Entity Relationship Diagram here](https://github.com/Jeetmajhi10/Revenue-Optimization-in-Hospitality-Sector/blob/0b524d902b77424248b6c9cf77bd99498a859a6c/Screenshot%202025-07-18%20184143.png)

# Executive Summary

### Overview of findings


