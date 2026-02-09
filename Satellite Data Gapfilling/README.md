Python-based Google Earth Engine (GEE) workflow to perform temporal gap filling of MODIS-Aqua Level-3 chlorophyll-a data. 

The method fills missing pixels by interpolating between the nearest valid observations before and after a target date within a defined temporal window.

##Study Area
ocean shape file is loaded from a Google Earth Engine Asset. You may replace this with your own shapefile/feature collection.

Dataset Used

MODIS-Aqua Level-3 Standard Mapped Image

Dataset ID:

NASA/OCEANDATA/MODIS-Aqua/L3SMI


Variable: chlor_a

Temporal coverage: 2002–2021

Spatial resolution: ~4 km

Methodology
1. Earth Engine Initialization

Authenticates and initializes GEE using a project ID

Uses geemap for visualization

2. Data Preparation

Filters by:

Date range

Region of interest

Clips images to ROI

Preserves original masks

3. Timestamp Handling

Adds acquisition time (system:time_start) as a masked image band

Enables pixel-wise temporal interpolation

4. Temporal Joining

Defines a ±200-day time window

Performs two joins:

Images before each target image

Images after each target image

5. Linear Interpolation

Computes interpolation ratio & interpolates pixel values. 

Replaces masked pixels only (original valid data preserved)

6. Output

Produces a gap-filled ImageCollection

Visualized as a mean chlorophyll map
