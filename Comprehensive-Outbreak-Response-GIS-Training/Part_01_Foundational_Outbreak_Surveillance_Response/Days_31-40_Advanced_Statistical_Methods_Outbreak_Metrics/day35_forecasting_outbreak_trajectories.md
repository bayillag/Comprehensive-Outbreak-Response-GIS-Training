# **Day 35 – Forecasting Outbreak Trajectories**
  
Bloom Level: Create & Apply | Duration: 4 hrs  

## Objectives  

- Explain principles of epidemic forecasting and uncertainty quantification.  
- Fit statistical time-series models (ARIMA, ETS) and evaluate forecast accuracy.  
- Build a simple mechanistic (SEIR) model for trajectory simulation and scenario analysis.  
- Compare and validate forecasting approaches using back-testing (sliding-window).  
- Communicate forecast outputs with prediction intervals and caveats.  

## Agenda  

1. Lecture: Forecasting Paradigms (45 min)  
   - Statistical models: ARIMA, exponential smoothing, Prophet  
   - Mechanistic models: compartmental SEIR basics  
   - Forecast horizons, uncertainty, and intervention scenarios  

2. Demo: Statistical Forecasting in R and Python (30 min)  
   - R: `forecast::auto.arima()`, `ets()` and `forecast()`  
   - Python: `statsmodels.tsa.arima`, `pmdarima.auto_arima`, `Prophet`  

3. Group Exercise: Time-Series Back-Testing (45 min)  
   - Create training/test splits with sliding window  
   - Fit ARIMA and ETS models; generate 14-day ahead forecasts  
   - Compute MAE and RMSE for each window  

4. Interactive Demo: SEIR Model Simulation (60 min)  
   - Implement SEIR in R (`deSolve`) or Python (`SciPy.integrate`)  
   - Calibrate transmission rate to early incidence data  
   - Simulate scenarios: no intervention vs. reduced contact rate  

5. Discussion & Q&A (30 min)  
   - Interpreting diverging model outputs  
   - Communicating uncertainty and limitations to stakeholders  
   - Choosing models based on data availability and operational needs  

---

## Exercise Details  

**Data Provided:**  
- `day35_daily_cases.csv`: time series of daily case counts  
- `day35_mobility.csv`: daily mobility index as covariate for transmission changes  
- `day35_seir_params.json`: default SEIR parameter values (β, γ, σ, N)  

**Key Tasks:**  
1. Prepare sliding-window splits (e.g., train on days 1–30, test on days 31–35).  
2. Fit ARIMA and ETS models, generate point forecasts and 95% prediction intervals.  
3. Calculate MAE and RMSE for each back-test window; summarize accuracy.  
4. Implement SEIR simulation, estimate β by fitting to the first two weeks, then project forward.  
5. Compare trajectories from statistical and mechanistic models; note divergence and uncertainty.  

---

## Assignment  

Submit to `assignments/day35/` by Day 36 morning:

1. Statistical Forecast Script (`day35_statistical_forecast.R` or `day35_statistical_forecast.py`)  
2. SEIR Simulation Script (`day35_seir_model.R` or `day35_seir_model.py`)  
3. Forecast Outputs (`day35_forecasts.csv`, `day35_seir_projection.csv`)  
4. Forecast Plots (`day35_forecast_plot.png`)  
   - Time-series with observed data, point forecasts, and prediction intervals  
5. Analytical Report (`day35_report.md`)  
   - 400–500 words comparing model performance, interpretability, and scenario insights  
6. Reflection (`day35_reflection.md`)  
   - 200 words on challenges in outbreak forecasting and communicating uncertainty
