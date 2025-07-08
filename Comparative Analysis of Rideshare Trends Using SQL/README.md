# SQL Data Analysis Project: Ride-Sharing Case Study (Zuber Chicago)

## 📊 Project Overview

This project is a practical analytics case study simulating work for **Zuber**, a new ride-sharing company launching in Chicago. The goal was to explore passenger preferences and assess the impact of external factors—like weather—on ride frequency and duration. 

The project involved:
- Performing exploratory data analysis (EDA)
- Writing complex SQL queries
- Testing hypotheses about weather impacts on rides

This was completed as part of a capstone to demonstrate SQL skills acquired through a structured course.

---

## 🗂️ Data Description

The analysis was conducted on a relational database that contained four tables:

| Table             | Description                                        |
|-------------------|----------------------------------------------------|
| **neighborhoods**  | Chicago neighborhood data (`neighborhood_id`, `name`) |
| **cabs**           | Taxi vehicle data (`cab_id`, `company_name`, etc.) |
| **trips**          | Ride data (`trip_id`, `start_ts`, `duration`, etc.)|
| **weather_records**| Weather data (`ts`, `temperature`, `description`)  |

Note: There was no direct foreign key linking trips and weather, so time-based joins were used.

---

## 🔍 Key Analysis Steps

### 🚖 1. Exploratory Data Analysis
- **Taxi rides by company**: Found number of rides per taxi company for Nov 15-16, 2017, ordered by ride volume.
- **Filter by company name**: Calculated trips for companies containing "Yellow" or "Blue" from Nov 1-7, 2017.
- **Popular vs Other companies**: Isolated data for `Flash Cab` and `Taxi Affiliation Services`, grouping all others as "Other," to compare volumes.

### 🌧️ 2. Weather Impact on Ride Duration
- Identified `O'Hare` and `Loop` neighborhood IDs.
- Created a `weather_conditions` flag using `CASE`:
  - `"Bad"` if `description` included "rain" or "storm"
  - `"Good"` otherwise
- Retrieved rides starting in the `Loop` (pickup ID 50) and ending at `O'Hare` (dropoff ID 63) on Saturdays, merged with weather data by hour, and compared ride durations under different weather.

---

## 🛠️ Tools Used
- **SQL** (PostgreSQL-style syntax for joins, CASE, aggregation)
- **Relational database concepts** (grouping, filtering, multi-table joins)
- **Time-series matching** to join weather with rides

---

## 📸 Screenshots

See `SQL for Zuber Screenshots.pdf` for screenshots of the queries and outputs.

---

## ✅ Results & Insights

- Identified top-performing taxi companies by trip volume.
- Quantified how ride durations between the Loop and O’Hare changed under adverse weather on Saturdays, revealing the operational impact of rain or storms on trip times.

---

## 🚀 What I Learned

- Advanced use of `CASE` statements and conditional aggregation.
- Joining tables without explicit foreign keys using timestamps.
- Translating business questions into efficient SQL queries.

---

📌 *This project is a simulated case study for educational purposes to showcase SQL data analysis skills.*

