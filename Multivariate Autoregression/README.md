# Multivariate Autoregression of Algal Bloom Intensity Prediction

The workflow produces spatial regression coefficients that describe how SST, salinity, SSH, precipitation, POC, and wind speed influence variability of bloom intensity.

## Dataset Used
- Chlorophyll: MODISAqua L3SMI
- Temperature: MODISAqua L3SMI
- Particulate organic carbon: MODISAqua L3SMI
- precipitation: GPM IMERG
- salinity: HYCOM
- sealevel: HYCOM
- Windspeed: NOAA Pathfinder

## Methodology
1. Monthly Composites-
Temporal aggregation (mean or max)

Clipped to study region

3. Bloom Detection-
Binary bloom mask generated for each month

4. Linear Detrending-
Trend removed to isolate variability component

5. Lagged Correlation-
Time-lag join between bloom and SST

Covariance matrix reduced to Pearson correlation

7. Multivariate Autoregression-
Spatial regression coefficients computed per pixel

8. Spatial Smoothing-
Neighborhood averaging using circular kernel

## Requirements
- Python ≥ 3.9

- Google Earth Engine Python API

- geemap
