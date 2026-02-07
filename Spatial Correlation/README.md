# Chlorophyll Bloom Detection and Identifying its Correlation (lagged) with Sea Surface Temperature

## Key Objectives

* Detect bloom events using MODIS-Aqua chlorophyll

* Identify and label spatially connected bloom patches

* Compute bloom intensity (highest concentration) per bloom patch

* Remove long-term trends using linear detrending

* Quantify lagged cross-correlation between blooms and SST

* Export correlation maps

## Study Area

The region of interest (ROI) is defined using a user-uploaded Earth Engine asset. You must replace this asset with your own Earth Engine FeatureCollection.

## Datasets Used
Chlorophyll-a : MODISAqua L3SMI
SST: MODISAqua L3SMI
Time period: January 2003 – December 2020

## Methodology Overview
1. Monthly Compositing using calendar filters in GEE

2. Bloom Detection using Chlorophyll bloom threshold

3. Connected bloom pixels are grouped & Mean chlorophyll is calculated per bloom patch 

4. Time Variable Construction (A constant band is added for regression)

5. De-trending using Ordinary least squares regression

6. Lagged Cross-Correlation: Bloom intensity data are lagged relative to SST by 31 days. 
Covariance matrix & Pearson correlation coefficient is derived

7. Final lagged correlation map is exported to Google Drive
