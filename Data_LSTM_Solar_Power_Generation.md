# Data Sources

This project uses openly available datasets from the [Open Power System Data (OPSD)](https://data.open-power-system-data.org/) platform.  
Due to file size limitations, the raw CSVs are not included in this repository.  
Instead, please download them directly from the sources listed below.

---

## 1. Weather Data
- **Source**: [OPSD Weather Data (2020-09-16)](https://data.open-power-system-data.org/weather_data/2020-09-16)  
- **Description**:  
  This dataset contains radiation and temperature data at hourly resolution for Europe.  
  The data was aggregated by *Renewables.ninja* from the NASA MERRA-2 reanalysis and covers European countries using a population-weighted mean across all MERRA-2 grid cells within each country.  

---

## 2. Solar Power Generation Data
- **Source**: [OPSD Time Series (2020-10-06)](https://data.open-power-system-data.org/time_series/2020-10-06)  
- **Description**:  
  This dataset contains time series relevant for power system modelling, including electricity prices, consumption (load), wind and solar power generation, and capacities.  
  - Aggregated by country, control area, or bidding zone.  
  - **Resolution**: Hourly (with separate files for half-hourly and quarter-hourly data where available).  
  - **Coverage**: EU and neighboring countries.  
  - **Period used in this project**: 2015–2019.  
  - Data is primarily provided by TSOs and power exchanges via ENTSO-E Transparency.  

---

## Notes
- Both datasets were preprocessed (cleaning, merging, normalization) before being used in the LSTM model.  
- For details on preprocessing, see the notebook in the repository