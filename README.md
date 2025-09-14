# Solar Power Generation Forecasting with LSTM

## 1. Overview
This machine learning project forecasts solar power generation in Germany using weather data and Long Short-Term Memory (LSTM) neural networks for 24-hour ahead predictions. The analysis explores the relationship between meteorological conditions and solar power output, developing a robust forecasting model suitable for grid operations and energy trading applications.

The project demonstrates how deep learning techniques can be applied to renewable energy forecasting, achieving strong predictive performance with an R² of 0.92 on day-ahead predictions.

## 2.  Dataset
### 2.1 Source

### Weather Data
The weather data was obtained from [Open Power System Data – Weather Data](https://data.open-power-system-data.org/weather_data/2020-09-16).  
This dataset contains radiation and temperature data at hourly resolution for Europe, aggregated by Renewables.ninja from the NASA MERRA-2 reanalysis.  
Coverage is provided for European countries using a population-weighted mean across all MERRA-2 grid cells within each country.

### Solar Power Generation Data
The solar power generation data was obtained from [Open Power System Data – Time Series](https://data.open-power-system-data.org/time_series/2020-10-06).  
This dataset includes time series relevant for power system modelling, such as electricity prices, electricity consumption (load), wind, and solar power generation and capacities.  
Data is aggregated by country, control area, or bidding zone, with hourly resolution. When original data is available in higher resolution (half-hourly or quarter-hourly), it is provided in separate files.  

This dataset version contains data provided by TSOs and power exchanges via ENTSO-E Transparency, covering the period 2015 to mid-2020. Previous versions include historical data from a broader range of sources.

### 2.2 Dataset Structure
The dataset contains the following key variables:

- Datetime: timestamp for each observation (hourly frequency)  
- Solar Power Generation: actual solar power output in megawatts (MW)  
- Direct Solar Radiation: direct normal irradiance measurements  
- Temperature: ambient temperature readings in degrees Celsius  
- Additional Weather Variables: supporting meteorological data including humidity, wind speed, and cloud cover  
- Seasonal Indicators: derived features for time-based patterns  


## 3. Analysis

### 3.1 Tools Used in the Analysis
- Python 3.x  
- Pandas: data manipulation and time series processing  
- NumPy: numerical computations and array operations  
- Matplotlib/Seaborn: data visualization and result plotting  
- Scikit-learn: data preprocessing, scaling, and evaluation metrics
- TensorFlow/Keras: LSTM model development and training  


### 3.2 Structure of the Analysis
- Exploratory Data Analysis: examination of solar generation patterns, weather correlations, and seasonal trends  
- Data Preprocessing: feature scaling, sequence creation for LSTM input, and train/validation/test splits  
- Model Development: LSTM architecture design with dropout regularization and batch normalization  
- Model Training: optimization with early stopping and learning rate scheduling to prevent overfitting  
- Performance Evaluation: comprehensive assessment using multiple metrics and visualization of predictions vs. actual values  

### 3.3 Key Findings
- Strong Predictive Performance: Final model achieves R² = 0.92 on test data 
- Excellent Generalization: No overfitting detected, with test performance exceeding training metrics  
- Weather Dependency: Direct solar radiation emerges as the strongest predictor of solar power generation  
- Temporal Pattern Capture: LSTM effectively learns diurnal cycles and seasonal variations in solar output
- Forecasts demonstrate practical applicability for day-ahead solar energy planning


### 4. Usage/Installation

- 1. Clone the repository
     
     git clone https://github.com/lilalaser/Python-LSTM-Solar-Power-Generation.git

- 2. Move into the project directory
     
    cd Python-LSTM-Solar-Power-Generation

- 3. Install required Python libraries (pandas, numpy, etc. ).
- 4. Run the Jupyter Notebook for analysis.


### 5. Contact

For questions or contributions, please open an issue or pull request on GitHub.
