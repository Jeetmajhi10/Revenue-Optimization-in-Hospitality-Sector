# Project Background
 In the competitive and dynamic hospitality industry, hotels and resorts frequently encounter
 revenue leakages, underutilized capacity, and fluctuating profitability. These challenges arise
 due to factors such as inefficient pricing strategies, inconsistent demand across weekdays and
 weekends, underperformance of specific room types or service offerings, and lack of actionable
 insights from available customer and booking data.
 
This project, undertaken as part of the **Consulting & Analytics Club at IIT Guwahati**, directly confronts these challenges. It presents an end-to-end analytical framework designed to help AtliQ Hotels, a leading hotel chain, identify the root causes of revenue leakage. By leveraging a comprehensive historical dataset, the analysis uncovers critical inefficiencies and proposes data-backed strategies to optimize pricing, enhance product offerings, and improve overall profitability. The final output is not just a report, but a strategic roadmap for informed, data-driven decision-making.

 Insights and recommendations are provided on the following key areas:

 - **Revenue Trend Analysis:**  Evaluation of historical revenue patterns, both by property name and by region, focusing on RevPar and Average Daily Revenue (ADR).
 - **Bookings Analysis:**  Distribution of bookings across room class, platform, and day type, understanding the reason behind revenue leakage.
 - **Generated vs Realized:**  An evaluation of actual revenue realized by the properties and how deviated it is from the revenue generated.
 - **What‑If ROI Simulator:**  Models how modest increases in premium bundling, cancellation mitigation, or direct‑booking shifts can recapture millions and improve ROI up to ~2%.

An interactive Power BI dashboard used to analyze and explore the above-mentioned insights can be found here. [link](https://app.powerbi.com/groups/me/reports/0be65715-f1d4-4d39-bb05-89f79e85f4bb/1781d5352c50911cbc29?experience=power-bi)


# Data Structure & Initial Checks
The company's main database structure, as seen below, consists of four tables:
- **134,000+** individual booking records.
- 7 distinct properties across major cities.
- 4 different room classes (Standard, Elite, Premium, Presidential).
- 7 unique booking platforms, including Online Travel Agencies (OTAs) and direct channels.
  
![Entity Relationship Diagram here](https://github.com/Jeetmajhi10/Revenue-Optimization-in-Hospitality-Sector/blob/0b524d902b77424248b6c9cf77bd99498a859a6c/Screenshot%202025-07-18%20184143.png)

# Executive Summary

### Overview of findings

- **Suboptimal Revenue Mix**: Weekdays contributed 69.35% of bookings and 1185M in revenue. Weekend bookings, though fewer, showed higher ADR (12,725) and better occupancy (62.6%) than weekdays (55.9%). The hotel operates a high-volume, lower-margin business during the week and transitions to a higher-value, better-utilized model on weekends. ADR dips have been observed in week 19, week 22, and week 24. This suggests that weekday demand is more price-sensitive and that there is an opportunity to introduce value-driven offerings to boost weekday ADR and occupancy. 

![line-chart](https://github.com/Jeetmajhi10/Revenue-Optimization-in-Hospitality-Sector/blob/bbd2fbab6b6a4f523e14cf2ed07c27f45ca9fc91/Screenshot%202025-07-22%20164636.png) ![Booking analysis](https://github.com/Jeetmajhi10/Revenue-Optimization-in-Hospitality-Sector/blob/94d6fb20489855d3ef19c70e5045f279810652be/Screenshot%202025-07-22%20122737.png) 

- **Cancellation-Driven Revenue Loss**: Over ₹299 Million in potential revenue was lost to cancellations within the 3-month period. A staggering 64% of this loss is attributable to last-minute cancellations, signaling flawed booking policies.

![last-minute](https://github.com/Jeetmajhi10/Revenue-Optimization-in-Hospitality-Sector/blob/2c90de8189b96d94fc1a226f60ca57aa1efb77a1/Screenshot%202025-07-22%20121105.png)

- **Underperformance of Premium Assets**: Premium and Presidential rooms, with high ADRs of ₹15,120 and ₹23,440 respectively, contribute over ₹839M combined. However, their occupancy rate (~58-59%) is only marginally better than that of standard rooms. The flat Realization Rate (~70%) across all room types indicates that premium pricing is not translating into better booking commitment or perceived value. The reason can be because guests are not sufficiently incentivized to choose premium offerings. The value proposition is unclear, leading to the underutilization of the hotel's most valuable inventory. This points to a failure in product bundling, marketing, and upselling.

![Table](https://github.com/Jeetmajhi10/Revenue-Optimization-in-Hospitality-Sector/blob/0730a167c3f7b377e89d25f620ec90c391e6820d/Screenshot%202025-07-22%20162641.png) ![Class-performance](https://github.com/Jeetmajhi10/Revenue-Optimization-in-Hospitality-Sector/blob/324c56923ab8b12cbd5879ff6d2168ad8f7ed3c8/Screenshot%202025-07-22%20161711.png)  

- **Customer & Channel Dynamics**: The "Budget" customer segment (ADR ~₹7,416) is responsible for 47,545 bookings but suffers from a 46% cancellation rate, making it a significant leakage zone. In stark contrast, the "Luxury" segment (ADR ~₹30,903) has a 0% cancellation rate, representing the most reliable customer base. The hotel's flexible booking policies, particularly on OTA platforms like makeyourtrip and tripster, attract a high volume of low-commitment "bargain-hunting" traffic that frequently cancels. The business is paying high commissions to OTAs for low-quality bookings while failing to cultivate its most valuable direct customers.

- **Property-wise Analysis**: Atliq Exotica and Atliq Palace had the highest total revenue (320M and 304M respectively), with solid RevPAR and stable ADRs. Atliq Blu had the highest occupancy (62.02%) and a low cancellation rate. In contrast, Atliq Seasons had the lowest occupancy (44.62%) and the lowest rating (2.29), indicating poor customer experience and/or demand misalignment.

![Property](https://github.com/Jeetmajhi10/Revenue-Optimization-in-Hospitality-Sector/blob/f8e9d3860efdc9afa3e34042735a9b2345b9dad0/Screenshot%202025-07-22%20163610.png) ![analysis](https://github.com/Jeetmajhi10/Revenue-Optimization-in-Hospitality-Sector/blob/f94d47dbf8b0a915ce895d81267e17cbe8ee914b/Screenshot%202025-07-22%20163648.png)

# Recommendations 

- **Implement Premium Room Bundling**: Address the underperformance of premium rooms by creating bundled packages that include value-added services like complimentary breakfast, spa credits, late checkout, or airport transfers. A package priced at $500 is projected to generate an additional ₹4.66M in monthly revenue at a 10% adoption rate.
- **Introduce Dynamic Cancellation Policies**: Mitigate revenue loss from last-minute cancellations by implementing a tiered cancellation policy. This involves introducing non-refundable or partially refundable rates for bookings cancelled within a 72-hour window before check-in. This strategy disincentivizes speculative bookings from low-commitment customers, particularly from OTA channels, and secures revenue that would otherwise be lost. This policy is projected to recover ₹13.56M in monthly revenue at a 10% uptake.
- **Drive Direct Bookings to Improve Margins**: Reduce dependency on high-commission OTAs by launching a "Book Direct" campaign. This involves offering exclusive perks—such as free Wi-Fi, meal credits, or loyalty points—to guests who book directly through the hotel's website or app. This shifts booking volume from high-cost channels to a zero-commission direct channel, leading to a direct improvement in profit margins for every converted booking. Shifting just 10% of OTA bookings to direct channels is projected to save ₹15.09M in monthly commission fees. 

![Revenue-impact](https://github.com/Jeetmajhi10/Revenue-Optimization-in-Hospitality-Sector/blob/93791d5211e003951abbaa7be1e52d9efde5261a/Screenshot%202025-07-22%20172213.png)


