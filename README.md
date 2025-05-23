# 🌍 Capstone Project: Weather Analysis

## 📁 Overview

This repository presents an in-depth analysis of global weather patterns using structured datasets stored in SQL and enhanced with Excel and Power BI for visualization. The goal of the project is to identify trends, seasonal behavior, geographical relationships, and weather-driven impacts by analyzing key meteorological variables such as temperature, humidity, air pressure, wind speed, wind direction, and descriptive weather conditions.

---

## 🗃️ Dataset Description

The project utilizes a relational database with the following tables:

### **1. city\_attributes**

* **Purpose**: Contains geospatial metadata for each city.
* **Columns**: `Country_id`, `City_id`, `Latitude`, `Longitude`
* **Usage**: Used to identify geographical trends, clustering, and regional impacts.

### **2. city\_lookup**

* **Purpose**: Maps city IDs to their names.
* **Columns**: `City_id`, `City`

### **3. country**

* **Purpose**: Maps country IDs to country names.
* **Columns**: `Country_id`, `Country`

### **4. date\_lookup**

* **Purpose**: Stores date information.
* **Columns**: `date_id`, `date`

### **5. time\_lookup**

* **Purpose**: Stores time information.
* **Columns**: `time_id`, `time`

### **6. final\_fact**

* **Purpose**: Main fact table with all weather data.
* **Columns**: `City_id`, `date_id`, `time_id`, `humidity`, `pressure`, `temperature`, `weather_description`, `wind_direction`, `wind_speed`
* **Usage**: Central to all EDA and dashboard analysis.

---

## 🔍 MECE Breakdown

### Mutually Exclusive Categories:

* **Geographical Analysis**: Using latitude, longitude, and clustering logic.
* **Weather Attributes**: Temperature, humidity, pressure, wind speed, wind direction.
* **Temporal Analysis**: Patterns by hour, month, and season.
* **Impact Analysis**: Pollution dispersion, energy use, extreme weather impact.

### Collectively Exhaustive Coverage:

* **City-Level Climate Profiling**
* **Correlation Studies Between Variables**
* **Detection of Anomalies and Events**
* **Predictive Insights for Planning & Resilience**

---

## 🧪 Exploratory Data Analysis (EDA) – MySQL + Excel

All EDA questions were solved using SQL queries run on the relational dataset. Results were exported to Excel for tabular representation and basic charts.

### EDA Questions and Analysis:

1. **Extreme Latitude Cities** – No cities above 60°N or below 60°S → Polar climates not included.
2. **Geolocation Clusters** – Grouped cities with lat/lon difference < 1° show similar climates.
3. **Geo-Weather Correlation** – Latitude correlates negatively with temperature; longitude correlation is weak.
4. **Rainiest Cities** – Toronto, Montreal, Vancouver; rains peak in spring and fall.
5. **Humidity vs. Pressure** – Weak correlation, mostly stable pressure and high humidity.
6. **Wind Direction Impact** – Coastal wind directions influence city temperature patterns.
7. **Seasonal Temperature Fluctuations** – February shows largest fluctuation (up to 36°C).
8. **Extreme Weather Events** – Peak storm activity in April; heatwaves common in May-July.
9. **Hemisphere Comparison** – Southern Hemisphere warmer in NH winters; both show warming trend.
10. **Extreme Heat Adaptation** – Cities face health/stress risks; adopt urban cooling and hydration strategies.
11. **Temperature Anomalies** – Spikes in San Diego, Las Vegas, and Miami linked to urban heat or weather shifts.
12. **Energy Consumption Link** – Strong positive correlation with temperature; higher temp = more energy use.
13. **Wind and Pollution** – Steady wind helps disperse pollutants; stagnant patterns trap pollution.
14. **Wind-Prone Cities** – Dallas, Phoenix, San Diego show high wind risk and transport disruption.
15. **Wind vs. Weather Severity** – No direct correlation in coastal cities; inland winds higher in some cases.

---

## 📊 Power BI Dashboard Insights

The weather dataset was modeled in Power BI, and DAX was used to create calculated fields and time-series insights. Each visual addresses a key analytical question:

### Visual Questions & Insights:

1. **Geographical Map** – Visual distribution of cities using lat/lon.
2. **Bar Chart** – Top 10 countries by number of cities.
3. **Scatter Plot** – City latitudes grouped by continent.
4. **Line Chart** – Temperature trends from 2012 to 2017 for selected cities.
5. **Heatmap** – Humidity variation across cities and months.
6. **Time-Series Chart** – Wind speed vs. air pressure; inverse relation noted in 2016.
7. **Overall Temp Trend** – Rise from 285.46 K (2012) to 290.17 K (2017).
8. **Hourly Weather Heatmap** – Shows common times for “clear” or “rainy” conditions.
9. **Radial Chart** – Wind speed patterns by day of the week; highest on Tuesday/Thursday.
10. **City Comparison** – Comparative temperature trends between two cities (requires both).
11. **Country Heatmap** – Color-coded national average temperatures.
12. **Bar Chart** – Warmest: Miami, Eilat, Phoenix; Coldest: Montreal, Toronto.
13. **Wind Rose Chart** – Uniform wind direction data for selected cities.
14. **Wind Speed Heatmap** – Monthly average wind speed distribution across cities.
15. **Scatter Plot** – Wind speed vs. air pressure; used to detect storm conditions.

---

## ⚙️ How to Use This Repository

### Step 1: Data Loading

* Import `.csv` files or `.sql` dump into MySQL.
* Normalize and structure as per schema.

### Step 2: Run SQL Queries

* Write queries for EDA.
* Export results to Excel for further analysis.

### Step 3: Excel Analytics

* Create pivot tables, summaries, and charts.
* Analyze trends and anomalies.

### Step 4: Power BI Dashboarding

* Load all data into Power BI.
* Create relationships between tables.
* Build visuals using drag/drop and custom DAX formulas.

### Step 5: Reporting

* Compile key insights in slides or reports.
* Present findings with supporting charts and dashboards.

---

## 🛠️ Tools Used

| Tool     | Purpose                                      |
| -------- | -------------------------------------------- |
| MySQL    | Data extraction, joins, correlation analysis |
| Excel    | Query result analysis, early visualizations  |
| Power BI | Dashboard creation, DAX metrics, visuals     |

---

## 📌 Conclusion

This weather analytics project offers a structured methodology for extracting and visualizing meteorological insights. By combining SQL for deep data mining, Excel for summarization, and Power BI for visualization, the project provides actionable findings in urban planning, energy forecasting, and disaster preparedness.

Future extensions can include:

* Real-time data integration via APIs
* Multi-year trend forecasting
* Climate change indicators analysis


