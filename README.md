# UN Data Visualization Project
Project 2 of the Databases II Coursework. Project created and worked from May to June 2023.
A three-part data processing and visualization pipeline that extracts statistics from the United Nations data portal, processes them with Hadoop MapReduce jobs, stores results in MongoDB, and exposes an interactive web application for exploration.

## Table of Contents

- [Project Overview](#project-overview)  
- [Features](#features)   
- [Hadoop Calculations](#hadoop-calculations)  
- [Custom Analyses](#custom-analyses)  

## Project Overview

This project implements:

1. **Web Crawler**  
   - Scrapes UN data from [data.un.org/Explorer.aspx](http://data.un.org/Explorer.aspx).  
   - Retrieves homicide statistics (total and by sex), WHO health statistics, and tourism data.

2. **Hadoop MapReduce Jobs**  
   - Processes crawler output to compute aggregated metrics.  
   - Loads results into a MongoDB database for querying.

3. **Web Application**  
   - Dashboard that reads from MongoDB and renders interactive charts.  
   - Allows filtering by dimensions (country, year, decade, sex, economic quintile, etc.).

## Features

- **Automated Data Extraction**  
- **Distributed Data Processing** with Hadoop  
- **Non-Relational Storage** in MongoDB  
- **Interactive Visualizations** using D3.js  

## Hadoop Calculations
The following metrics are computed via Hadoop MapReduce jobs:

1. **Average homicide victims per country**  
2. **Average, max, and min homicides by region per year**  
3. **Average, max, and min homicides by sub‑region per year**  
4. **Average homicide victims per country by sex**  
5. **Average, max, and min homicides by region and sex per year**  
6. **Average, max, and min homicides by sub‑region and sex per year**  
7. **Average, max, and min homicides by region and sex per decade**  
8. **Average, max, and min homicides by sub‑region and sex per decade**  
9. **Percentage of deaths (age 30–70) by country & year for:**  
   - Cancer vs. total  
   - Cardiovascular diseases vs. total  
   - Respiratory diseases vs. total  
10. **Average, max, and min deaths per country for:**  
    - Reported causes  
    - Unreported causes  
    - Injuries  
11. **Difference between first and last measured average age per country**  
12. **Average age per country per decade**  
13. **Population count per decade**  
14. **Adolescent fertility rate (per 1,000) by country & decade**  
15. **Adolescent fertility rate (per 1,000) by economic quintile, country & decade**  
16. **Under‑one infant mortality rate (per 1,000) by country & decade**  
17. **Under‑one infant mortality rate (per 1,000) by quintile, country & decade**  
18. **Fertility rate by decade per country**  
19. **Total health expenditure by country & decade**  
20. **Health expenditure as % of government budget by country & decade**  
21. **Life expectancy at birth by country & decade**  
22. **Total inbound tourists by country & decade**  
23. **Total outbound tourists by country & decade**

## Custom Analyses
The following additional metrics are computed via Hadoop MapReduce jobs:

24. **Total homicide victims per country (2000–2020)**  
25. **Total homicide victims per region per year (2000–2020)**  
26. **Total homicide victims per sub‑region per year (2000–2020)**  
27. **Total homicide victims per region, year, and sex (2001–2021)**  
28. **Total homicide victims per sub‑region, year, and sex (2001–2021)**
