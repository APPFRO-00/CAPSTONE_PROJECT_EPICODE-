# CAPSTONE_PROJECT_EPICODE-
# 🏎️ Formula 1 Performance Analysis  
### Hybrid Era vs Ground Effect Era (2014–2025)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![ETL](https://img.shields.io/badge/ETL-Pipeline-orange)
![Data Modeling](https://img.shields.io/badge/Data%20Modeling-Star%20Schema-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 🎯 Project Goal

This project aims to analyze the evolution of performance in Formula 1 from 2014 to today, focusing on drivers, teams, and the impact of regulatory changes.

The analysis is based on building a clean and optimized data model, integrated into Power BI, to generate clear insights and effective visualizations.

---

## 🧩 Datasets

The data comes from a historical dataset available on Kaggle:  
👉 https://www.kaggle.com/datasets/rockyt07/formula-1-championships-1950-2025

### Main datasets used:

- **races.csv** → race information (year, circuit, date)  
- **results.csv** → complete race results per driver  
- **drivers.csv** → drivers registry  
- **constructors.csv** → teams registry  
- **constructors_champion.csv** → championship-winning teams  
- **drivers_champions.csv** → championship-winning drivers  

---

## 🛠️ ETL Process (Extract – Transform – Load)

### 🔹 Extraction
- Imported CSV files using **Pandas**
- Performed Exploratory Data Analysis (EDA):
  - `head()`
  - `describe()`
  - `info()`
  - null values check  

---

### 🔹 Transformation

- Removed duplicates across all datasets  
- Standardized column names (`DriverID`, `ConstructorID`, `RaceID`)  
- Converted data types (dates, numeric values, positions)  
- Filtered data from **2014 onward** (Hybrid Era start)  
- Dropped unnecessary columns (e.g., `Position`, keeping `PositionOrder`)  
- Created cleaned datasets:
  - `races_clean`
  - `results_clean`
  - `drivers_clean`
  - `constructors_clean`
- Applied dynamic filtering for active drivers and constructors  

---

### 🔹 Loading

- Saved cleaned datasets into a dedicated folder  
- Imported data into **Power BI** for modeling  

---

## 🧱 Data Model

Star Schema structure:

- **Fact Table**
  - `results_clean`

- **Dimension Tables**
  - `drivers_clean`
  - `constructors_clean`
  - `races_clean`

### Relationships:
- Results → Drivers (`DriverID`)  
- Results → Constructors (`ConstructorID`)  
- Results → Races (`RaceID`)  

---

## 📊 Analysis & Insights

The model allows:

- Driver performance analysis (wins, podiums, points, avg positions)  
- Team performance evaluation (titles, consistency, reliability)  
- Regulation impact comparison:
  - Hybrid Era (2014–2021)  
  - Ground Effect Era (2022–2025)  
- Driver vs driver / team vs team comparisons  
- Seasonal and multi-season trends  
- Retirement analysis using `Status`  
- Race movement (grid vs finishing position)  

---

## 🧠 Skills Demonstrated

- Advanced **ETL with Python & Pandas**  
- Data modeling with **Star Schema**  
- Analytical thinking & statistical analysis  
- Interactive dashboard development with **Power BI**  
- Data quality and consistency management  

---

## 🚀 Project Type

✔️ End-to-End Data Project  
✔️ Data Engineering + Data Analysis + Data Visualization  

---

## 📌 Future Improvements

- Add live data integration (API)  
- Enhance predictive analytics  
- Expand dashboard interactivity  

---
