# Data Folder

This folder contains the NTSB Aviation Accident Database and related documentation used for predictive modeling analysis. The working directory loads data automatically; no manual preprocessing is required.

## Data Source  
- **National Transportation Safety Board (NTSB) Aviation Accident Database**  
- **URL:** [https://www.ntsb.gov/safety/data/Pages/Data_Stats.aspx]
- **Coverage:** Commercial aviation accidents (FAR Part 121 and 135 operations)  
- **Time period:** 2008–2024  
- **Observations:** 1,388 accident records  

## Key Variables  

- **Outcome Variable:**  
  - `fatal` — Binary indicator (1 = at least one fatality, 0 = no fatalities)  

- **Operational Context:**  
  - `far_part` — Regulatory classification (121: Scheduled Airlines, 135: Air Taxi & Commuter)  
  - `phase_group` — Flight phase (e.g., Standing/Parking, Taxi, Takeoff, Initial Climb, En Route, Descent, Unknown/Other)  

- **Human Factors:**  
  - `crew_age` — Pilot age (years)  
  - `crew_cat` — Crew category (Pilot, Co-pilot)  
  - `crew_sex` — Crew sex (Male, Female)  
  - `med_cert` — Medical certificate class (Class 1, Class 2)  

- **Environmental Conditions:**  
  - `wx_cond` — Weather condition (VMC: Visual, IMC: Instrument Meteorological Conditions)  
  - `visibility` — Visibility distance (miles)  
  - `temperature` — Ambient temperature (°C)  
  - `wind_speed` — Wind speed (knots)  

- **Temporal and Spatial:**  
  - `event_year` — Accident year  
  - `event_time` — Time of accident (24-hour format)  
  - `latitude`, `longitude` — Geographic coordinates  

## Missing Data  

Missing data rates vary by variable (0–45%). All missing values were imputed using Multiple Imputation by Chained Equations (MICE) in the analysis script. See the data dictionary for detailed missingness patterns.

## Usage  

Data files are loaded automatically in `Final_Report_[Pham].qmd`. Do not modify the raw data files; all transformations occur programmatically within the analysis script.
