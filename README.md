# Ride-Hailing-Market-Weather-Impact-Analysis-Chicago-
Analyse Chicago taxi market patterns and test whether rainy Saturdays affect trip duration from the Loop to O’Hare using SQL and Python.

## Objective
Analyse Chicago taxi trip data to identify competitor patterns and test whether weather conditions affect trip duration from the Loop to O’Hare on Saturdays.

## Overview
This project analyses Chicago taxi trip data to understand competitor market patterns and quantify the impact of weather on trip duration. The work combines SQL for data extraction and Python for exploratory analysis, visualisation, and hypothesis testing.

## Data
Database tables:
- neighborhoods (neighborhood_id, name)
- cabs (cab_id, vehicle_id, company_name)
- trips (trip_id, cab_id, start_ts, end_ts, duration_seconds, distance_miles, pickup_location_id, dropoff_location_id)
- weather_records (ts, temperature, description)

External source:
- Chicago weather (Nov 2017) scraped from a provided webpage

CSV outputs for Python analysis:
- project_sql_result_01.csv (company_name, trips_amount)
- project_sql_result_04.csv (dropoff_location_name, average_trips)
- project_sql_result_07.csv (start_ts, weather_conditions, duration_seconds)

## Key Questions
- Which taxi companies lead in trip volume during selected periods?
- Which drop-off neighborhoods receive the highest average number of trips?
- Do rainy Saturdays change average trip duration from the Loop to O’Hare?

## Workflow
1) Web data extraction: collect Chicago weather information for Nov 2017  
2) SQL analysis: company trip counts, grouping competitors, join trips with weather by timestamp  
3) Python EDA: import CSV outputs, validate types, top-10 locations, charts + interpretation  
4) Hypothesis testing: compare trip duration on “Bad” vs “Good” weather Saturdays

## Deliverables
- SQL queries (company-level analysis, weather classification, Loop → O’Hare trips)
- Charts: trips by company; top 10 drop-off neighborhoods
- Hypothesis test result with business interpretation

## 1. Data Extraction (Web)
Collect Chicago weather data for November 2017 from the provided webpage and prepare it for analysis.

## 2. SQL Analysis
### 2.1 Company trip volume
Compute trips per taxi company for defined date ranges and compare key competitors.

### 2.2 Market grouping
Report trips for Flash Cab and Taxi Affiliation Services, grouping all other companies as “Other”.

### 2.3 Weather classification
Create hourly weather labels:
- “Bad” if description contains rain or storm
- “Good” otherwise

### 2.4 Loop → O’Hare trips on Saturdays
Extract Saturday trips from Loop to O’Hare, attach weather conditions by matching timestamps, and keep trip durations.

## 3. Python EDA (CSV results)
Import SQL outputs, validate data types, identify top 10 drop-off neighborhoods, and visualise:
- trips by company (15–16 Nov 2017)
- top 10 neighborhoods by average drop-offs (Nov 2017)

## 4. Hypothesis Testing (Python)
Test whether average Loop → O’Hare trip duration differs on rainy (“Bad”) Saturdays vs non-rainy (“Good”) Saturdays.
Define H0/H1, choose alpha, run the statistical test, and interpret results in business terms.

## Conclusions
Summarise market insights (company concentration, top neighborhoods) and the impact of weather on trip duration, including implications for operations and forecasting.

## Tech
SQL, Python, pandas, matplotlib/plotly, scipy.stats, Jupyter Notebook

## Author
**Erika González**  
MBA | Marketing & Data Analytics  
Focus areas: Market Intelligence, Customer Behaviour, Statistical Analysis
