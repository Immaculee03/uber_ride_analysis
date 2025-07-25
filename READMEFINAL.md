#  Uber  Data Analysis with Python & Power BI

This project presents a comprehensive analysis of Uber ride fare patterns using Python (Pandas, Geopy) for data cleaning and feature engineering, and Power BI for interactive dashboard creation. The goal is to identify patterns, trends, and business insights from NYC Uber ride data.

---

##  Project Objectives

- Understand Uber ride fare data structure and quality
- Clean and preprocess the dataset for analysis
- Perform Exploratory Data Analysis (EDA)
- Engineer new analytical features
- Visualize key insights using Power BI
- Create an interactive dashboard for decision-making

---

##  Dataset Description

- **Source**: Uber Fares Dataset (Kaggle)
- **File Used**: `uber.csv` → cleaned and saved as `uber_enhanced_final.csv`
- **Fields included**:
  - `fare_amount`
  - `pickup_datetime`
  - `pickup_longitude`, `pickup_latitude`
  - `dropoff_longitude`, `dropoff_latitude`
  - `passenger_count`
  - Engineered fields: `hour`, `day`, `month`, `weekday`, `is_peak`, `distance_km`

---

##  Data Cleaning (Python)

Data was cleaned using Python in Kaggle Notebooks:

- Removed rows with missing values in key columns
- Removed invalid fare amounts (≤ 0 or ≥ 1000)
- Filtered coordinates to be within the NYC area
- Converted pickup time to datetime format
- Extracted `hour`, `day`, `month`, `weekday`, `year` from `pickup_datetime`
- Created `distance_km` using geodesic distance
- Added `is_peak` column for rush hour rides
- Applied one-hot encoding to the `weekday` column

>  Cleaned dataset exported as `uber_enhanced_final.csv` for Power BI import

---

##  Visualizations (Power BI)

The cleaned dataset was imported into Power BI to generate interactive visuals:

### Key Visuals Created:

- **Average Fare by Hour** (Line Chart)
- **Ride Volume by Hour** (Bar Chart)
- **Fare vs. Distance** (Scatter Plot)
- **Ride Volume: Peak vs Off-Peak** (Bar Chart)
- **Monthly Ride Patterns** (Column Chart)
- **KPI Cards**: Total Rides, Average Fare, Total Distance
- **Slicers**: Month, Hour, Passenger Count, Peak/Off-Peak
- *(Map visual skipped due to feature restrictions)*

>  Interactivity included via slicers and drill-downs

---

## Temporal Insights

- Higher fares during morning (7–9 AM) and evening (5–7 PM) peak hours
- Weekend rides showed more variability in fare and distance
- Distance is a strong predictor of fare amount

---

## Dashboard Overview

The Power BI Dashboard includes:
- Time-based patterns
- Distance-based fare analysis
- Key performance metrics
- User-friendly layout and filters for exploration

Power BI File: `uber_dashboard.pbix`

---

##  Project Structure
uber-ride-analysis/
│
├── data/
│ ├── uber_cleaned.csv
│ └── uber_enhanced_final.csv
│
├── screenshots/
│ ├── loading_data.png
│ ├── cleaning_part1.png
│ ├── cleaning_part2.png
│ ├── visuals_hourly.png
│ ├── visuals_distance.png
│ └── dashboard_final.png
│
├── powerbi/
│ └── uber_dashboard.pbix
│
└── README.md

---

## Key Insights

- Peak hours have higher fares on average
- Short-distance rides are more common, but long-distance rides bring higher fares
- Ride volume peaks in early mornings and late evenings

---

##  Recommendations

- Consider surge pricing or incentives during off-peak hours
- Optimize driver allocation during busiest hours and routes
- Analyze seasonal data in future versions (add weather if available)

---

##  Author

**Iradukunda Immaculee  27378**  
Project completed for academic submission using Python + Power BI  
2025

---


