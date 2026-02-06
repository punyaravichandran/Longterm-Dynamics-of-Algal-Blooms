# Summer Algal Bloom Trend Analysis (2003–2020)

This repository contains a Google Earth Engine (GEE)–based workflow to analyze **summer algal bloom dynamics** in the **Ocean** using **MODIS-Aqua chlorophyll-a** observations. The study focuses on identifying **bloom extent**, **long-term trends**, and **statistical significance**.

---

##  Objectives

- Quantify **summer (March–May) algal bloom area** using satellite chlorophyll-a
- Detect **long-term trends** in bloom extent (2003–2020)
- Estimate **trend magnitude** using **Sen’s slope**
- Assess **statistical significance** via the **Mann–Kendall test**

---

##  Study Region

- **Region:** Northern Indian Ocean  
- **Boundary:** User-defined polygon uploaded as a GEE asset  
- **Spatial Resolution:** ~6 km  

---

##  Dataset

**MODIS-Aqua Level-3 Standard Mapped Image (L3SMI)**  
- Product: `NASA/OCEANDATA/MODIS-Aqua/L3SMI`  
- Variable: `chlor_a` (chlorophyll-a concentration, mg m⁻³)  
- Temporal coverage: **2003–2020**  
- Seasonal filter: **March–May (summer)**  

---

##  Methodology

### 1. Bloom Detection
- Algal blooms are identified using a **fixed threshold**:

