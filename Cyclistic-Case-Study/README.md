# Cyclistic Bike-Share Analysis Case Study

## 1. Define the Problem
**Objective:** Cyclistic is analyzing the usage differences between its two types of users: **casual riders** and **annual members**. The goal is to differentiate these user patterns to create strategies that convert casual riders into annual members.

### Business Questions
* How do annual members and casual riders use Cyclistic bikes differently?
* How does the ride duration and volume differ for Casual and Annual members?
* What are the months with peak rides?

### Stakeholders
* Executive team
* Director of Marketing
* Marketing analytics team

---

## 2. Prepare Data
The data spans the past year (November 2024 to October 2025) and is stored in monthly CSV files.

**Source:** Data is collected from the [DivvyBikes website](https://www.divvybikes.com/system-data). It contains transaction records including `ride_id`, `member_type`, `station_name`, and `station_id`.

### Data Credibility (ROCCC Analysis)
| Attribute | Rating | Notes |
| :--- | :--- | :--- |
| **Reliable** | Medium | Data is not entirely consistent. |
| **Original** | High | First-party data source. |
| **Comprehensive** | Medium | Contains many null values. |
| **Current** | High | Up-to-date (Nov 2024 - Oct 2025). |
| **Cited** | Weak | Lacks detailed documentation. |

---

## 3. Process Data
To prepare the data for analysis, the following steps were taken:
1.  **Data Merging:** Combined all monthly CSV files into a single dataset using `ride_id`.
2.  **Standardization:** Ensured all data types were consistent (specifically date/time formats).
3.  **Feature Engineering:** Created new columns:
    * `ride_length`: Total duration of the trip.
    * `day_of_week`: The day the ride occurred.

---

## 4. Explore and Analyze Data
Exploratory Data Analysis (EDA) revealed the following patterns:

* **Ride Trends:** * **Casual Members:** Significant spikes during the weekend (Saturday–Sunday) and dips during the work week.
    * **Annual Members:** Higher volume during working days with a slight decrease on weekends.
* **Duration Trends:** * **Casual Members:** High average duration on weekends; lower on weekdays.
    * **Annual Members:** High average duration on weekdays; lower on weekends.

### Key Insights
> * **Volume:** Annual members have significantly higher ride counts than casual members, except on weekends.
> * **Duration:** Casual members' average ride duration is significantly higher than annual members across all days, peaking on weekends.

---

## 5. Visualize and Share Findings
Findings were presented to stakeholders using the following visualizations:
* **Line Charts:** Illustrated weekly peaks and troughs for both member types.
* **Bar Charts:** Highlighted total ride volume and average duration comparison.
* **Tableau Dashboard:** An interactive display for high-level insights at a glance.

---

## 6. Act on Results
Based on the analysis, the following data-driven strategies are recommended:

1.  **Weekend-Specific Membership Tier:** Offer a low monthly fee providing discounts or free rides for trips exceeding 60 minutes on Saturdays and Sundays.
2.  **Targeted Promotions:** Send weekend-member-specific promotions (e.g., 10% discount or ride credits) for weekend or mid-day weekday rides.
3.  **Optimized Maintenance & Redistribution:** * **Weekdays:** Focus redistribution on major commuter hubs in the afternoons.
    * **Weekends:** Deploy fleets near parks, tourist sites, and leisure areas.