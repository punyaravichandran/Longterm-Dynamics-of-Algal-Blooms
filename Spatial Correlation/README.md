Chlorophyll Bloom Detection and Climate Covariate Analysis

Detecting blooms and quantifying their lagged relationship with oceanographic variables (sea surface temperature).

Key Objectives

Detect bloom events using MODIS-Aqua chlorophyll

Identify and label spatially connected bloom patches

Compute bloom intensity (highest concentration) per bloom patch

Remove long-term trends using linear detrending

Quantify lagged cross-correlation between blooms and SST

Export correlation maps for further statistical analysis

Study Area

The region of interest (ROI) is defined using a user-uploaded Earth Engine asset. You must replace this asset with your own Earth Engine FeatureCollection.

Datasets Used
Chlorophyll-a : MODISAqua L3SMI
SST: MODISAqua L3SMI
Time period: January 2003 – December 2020
Temporal resolution: Monthly composites

Methodology Overview
1. Monthly Compositing
Implemented using calendar filters in Earth Engine

2. Bloom Detection
Chlorophyll bloom threshold. Binary bloom masks are created and self-masked

3. Object-Based Analysis
Connected bloom pixels are grouped. 

Maximum object size = 500 pixels

Mean chlorophyll is calculated per bloom object

4. Time Variable Construction
A constant band is added for regression modeling

5. De-trending
Linear trends are removed using Ordinary least squares regression

6. Lagged Cross-Correlation
Bloom intensity data are lagged relative to SST by 31 days

Covariance matrix is computed

Pearson correlation coefficient is derived

7. Export

Final lagged correlation map is exported to Google Drive
