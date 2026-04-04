# Broadband Accessibility Analysis in Manitoba Using QGIS

## Overview
This project analyzes broadband availability across Manitoba by integrating telecommunications data with 2021 Census demographics. The goal is to identify underserved regions where population levels are high relative to broadband access.

The analysis is conducted using QGIS and demonstrates how geospatial techniques can be applied to infrastructure and connectivity challenges at a provincial level.

## Objective
To identify underserved regions in Manitoba by:
- Integrating broadband availability data with census population data  
- Creating a metric to quantify gaps in connectivity  
- Visualizing underserved areas using geospatial mapping  

## Data Sources
- Broadband availability data from Innovation, Science and Economic Development Canada  
- 2021 Census population data from Statistics Canada  
- Census boundary shapefiles (CSD or DA level) filtered for Manitoba  

## Tools and Technologies
- QGIS  
- CSV datasets  
- Shapefiles  

## Methodology

### 1. Data Preparation
- Loaded census boundary shapefile into QGIS  
- Filtered dataset to include only Manitoba regions  
- Imported population and broadband datasets as CSV files  

### 2. Data Integration
- Joined population data to geographic boundaries using region identifiers  
- Joined broadband availability data to the same geographic layer  

### 3. Feature Engineering
Created a metric to estimate underserved regions:
underserved_score = population / broadband_availability


This metric highlights areas with higher population relative to connectivity.

### 4. Visualization
- Applied graduated symbology based on the underserved score  
- Used a color ramp to distinguish underserved and well-served areas  
- Generated a choropleth map focused on Manitoba  

## Results
The analysis identifies regions within Manitoba where broadband access may not adequately support population demand. These areas are highlighted through higher underserved scores in the visualization.

## Project Structure

.
├── data/
│ ├── broadband_data_mb.csv
│ ├── census_population_mb.csv
│ └── manitoba_boundaries.shp
├── outputs/
│ └── underserved_map_mb.png
└── README.md


## How to Reproduce

1. Open QGIS  
2. Load the Manitoba boundary shapefile  
3. Import CSV datasets  
4. Join datasets using geographic identifiers  
5. Create the underserved_score field using the Field Calculator  
6. Apply graduated symbology based on the new field  
7. Export the map as an image  

## Key Insights
- Certain regions in Manitoba show higher population-to-connectivity gaps  
- Regional-level analysis provides clearer insights than national aggregates  
- Geospatial techniques help identify infrastructure investment priorities  

## Future Improvements
- Incorporate additional variables such as income or rural classification  
- Use finer geographic granularity for deeper insights  
- Automate preprocessing using Python  
- Extend analysis to time-series data for trend evaluation  

## License
This project uses publicly available data and is intended for educational and analytical purposes.