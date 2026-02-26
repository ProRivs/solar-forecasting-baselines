# Purpose:

  This is documentation for the data folder only.
  
# It answers:

- What data belongs here?
  
- Where does it come from?
  
- What is included / excluded?
  
- What are licensing or privacy constraints?
  
- Why data may be missing from the repo
  
# This is critical because:

- Data is often large, restricted, or external
  
- You may not commit raw data to GitHub
  
- Reproducibility depends on data clarity

## Data Source
NASA POWER project (Hourly, native resolution).

## Location
Maroua, Cameroon  
Latitude: 10.6032  
Longitude: 14.3226  

## Date Range
01/01/2021 – 12/31/2025

## Variables
- ghi_wh_m2: ALLSKY_SFC_SW_DWN (Wh/m² per hour)
- temp_c: T2M (°C)

## Temporal Resolution
Hourly (Δt = 1 hour confirmed via timestamp differences).

## Missing Data (Approximate)
- Missing GHI values: ~1.75%
- Missing temperature values: ~0.00%
- Missing hourly timestamps: ~0.00%

Missing values were encoded as -999 and converted to NaN during preprocessing.

## Known Limitations
- NASA POWER provides satellite/reanalysis-derived irradiance estimates over a coarse grid cell.
- Local cloud dynamics and short-term variability may be smoothed compared to ground measurements.
- Results should be interpreted as methodological baselines rather than plant-level operational forecasts.