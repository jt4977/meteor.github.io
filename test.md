Proposal
================
al4771, cx2347, jh4977, km4071, xf2290
2025-11-05

### **Group Numbers**

Jingtong He(jh4977), Chuyuan Xu(cx2347), Anqi Li(al4771), Xiwei
Fu(xf2290), Kaicheng Mo(km4071)

### **Tentative Project Title**

### **Motivation**

In recent years, the impacts of climate variability and extreme weather
events have become increasingly evident across New York State.
Understanding local climatic patterns is essential not only for
environmental monitoring, but also for informing public health
preparedness, agricultural planning, and infrastructure resilience.
Despite the availability of rich meteorological datasets, there remains
a need for integrated analytical approaches that combine visualization,
statistical modeling, and predictive analysis to uncover underlying
patterns and trends in regional climate behavior.

This project aims to leverage five years of comprehensive weather data
from New York State to visualize and model key climatic variables such
as temperature, precipitation, and wind speed. Through interactive
spatial visualizations—such as precipitation heatmaps across
counties—and regression-based analyses, we will identify the major
meteorological and geographic factors that shape local weather dynamics.
Furthermore, by applying time-series forecasting models, we aim to
predict future climatic trends and provide data-driven insights that
could support regional planning and climate adaptation strategies.

Ultimately, this project seeks to demonstrate the power of data
analytics in translating complex weather information into actionable
knowledge, while showcasing technical proficiency in data cleaning,
visualization, regression modeling, and time-series forecasting.

### **Variable Introduction**

In the meteorology datasets from 2016-2020, each dataset includes the
following variables:  
   `county`: Federal Information Processing Series (FIPS), the id of the
counties;  
   `date`: date of the estimated meteorological variables;  
   `sph`: near-surface specific humidity (Mass fraction);  
   `vpd`: mean vapor pressure deficit (kPa);  
   `tmmn`: minimum near-surface air temperature (Kelvin);  
   `tmmx`: maximum near-surface air temperature (Kelvin);  
   `pr`: precipitation (mm, daily total);  
   `rmin`: minimum near-surface relative humidity (%);  
   `rmax`: maximum near-surface relative humidity (%);  
   `srad`: surface downwelling solar radiation (W/m^2);  
   `vs`: wind speed at 10m (m/s);  
   `th`: wind direction at 10m (degree).  
  
Key variables in `tl_2024_county` are:  
    `GEOID`: Current county identifier; a concatenation of current state
FIPS code and county FIPS code;  
    `STUSPS`: Current United States Postal Service (USPS) state
abbreviation;  
    `NAME`: Current state name;  
    `NAMELSAD`: Current name and the translated LSAD code for county;  
    `geometry`: the geological boundaries in the geometry of
multipolygon.  
  
Key variables in `tl_2020_state` are:  
    `STATEFP`: State FIPS code;  
    `STUSPS`: Current United States Postal Service (USPS) state
abbreviation;  
    `NAME`: Current county name.  

### **Intended Final Products**

### **Anticipated Data Sources**

The meteorology datasets were downloaded from [“Daily meteorological
Gridmet variables by United States administrative boundaries”, Harvard
Dataverse](https://doi.org/10.7910/DVN/FYTME3). To monitor the changing
patterns in the past seasons and years, meteorological data from 2016 to
2020 on the county level.  
  
Corresponding county information was downloaded from [tiger/line
Shapefiles](https://www.census.gov/cgi-bin/geo/shapefiles/index.php).
Due to the lapse in federal funding, portions of the [United States
Census Bureau](https://www.census.gov/) were unavailable.
`tl_2020_state` and `tl_2024_county` were downloaded to obtain
additional New York state and county information to facilitate further
visualizations and analysis.  

### **Planned Analyses/ Visualizations**

Exploratory Data Analysis. Describe spatial and temporal distributions
of temperature, precipitation, and wind speed using histograms, density
plots, seasonal subseries, calendar heatmaps, and county-level
choropleths. Quantify autocorrelation and inter-variable dependence via
correlation heatmaps and lagged correlations.

Spatiotemporal Association Modeling.  
Fit interpretable regression families (linear/GLM, mixed-effects) to
quantify associations between meteorological outcomes and geographic
climatic drivers, with county-level random effects where appropriate.
Use two-part models for precipitation. Report coefficient forest plots,
marginal effects, residual diagnostics, and space–time cross-validation
errors.

Forecasting & Predictive Evaluation. Build short-horizon forecasts with
rolling-origin evaluation. For extreme events, train parsimonious
classifiers. Evaluate with RMSE/MAE.

Visualization Deliverables. Standardized map suite like levels and
anomalies, seasonal and calendar plots, correlation and diagnostics,
coefficient and marginal-effect displays, forecast fan charts and
rolling-error summaries.

### **Coding Challenges**

### **Planned Timeline**

Phase I — Introduction & Framing (Early November) Goal: Establish the
analytic scope and motivation for a five‑year, New York State–focused
climate analysis.  
Deliverables: Background paragraphs, research questions, simple analysis
flow schematic.

Phase II — Data Cleaning & Harmonization (Early to Mid‑November) Goal:
Acquire and standardize public meteorological data; produce a single
analysis‑ready table keyed to geographic identifiers. Deliverables:
Cleaned dataset, data‑quality summary (coverage/missingness), brief data
dictionary.

Phase III — Exploratory Analysis & Visualization (Mid to Late November)
Goal: Describe spatial and temporal patterns in temperature,
precipitation, and wind speed to inform modeling.  
Deliverables: EDA portfolio (maps, heatmaps, seasonal plots) with short
captions.

Phase IV — Statistical & Predictive Modeling (Late November to Early
December) Goal: Fit an interpretable regression for associations and a
short‑horizon forecaster with uncertainty quantification.  
Deliverables: Model summary with diagnostics, forecast error or coverage
summary, brief limitations note.

Phase V — Results, Discussion & Integration (Early to Mid‑December)
Goal: Synthesize evidence into a coherent narrative with implications
for monitoring and resilience.  
Deliverables: Finalized figures, completed Results & Discussion,
compiled PDF + GitHub document.

### **Project Structure**
