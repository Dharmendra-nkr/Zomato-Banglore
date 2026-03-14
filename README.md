# Zomato Bangalore Data Analysis and Location Intelligence

This project is a complete data analysis and visualization workflow on the Bangalore Zomato dataset. It combines exploratory data analysis (EDA), feature engineering, geospatial mapping, and machine learning-ready preprocessing.

A key part of the work was geocoding restaurant addresses to latitude/longitude, and this geocoding task was handled by me directly to build location-based insights.

## Project Highlights

- Performed end-to-end analysis on 51,717 restaurant records.
- Built cleaned and transformed datasets for downstream analysis.
- Generated location intelligence outputs using geocoded address data.
- Created map-based and statistical visualizations.
- Prepared encoded data for modeling and ML experiments.

## Dataset and Processed Files

### Raw source

- zomato.csv (51,717 rows)
  - Main raw dataset with restaurant info such as name, location, cuisines, pricing, ratings, and votes.

### Intermediate and final analytical datasets

- address_zomato.csv (9,499 rows)
  - Cleaned address-focused subset for geocoding.
- addresses_with_coordinates.csv (9,499 rows)
  - Address-level data enriched with latitude and longitude.
- zomato_locations.csv (92 rows)
  - Aggregated/normalized location-level data.
- df_le.csv (41,263 rows)
  - Label-encoded dataset used for machine learning and correlation/model workflows.

## Notebooks and Their Roles

- zomato_part1.ipynb
  - Core EDA, visual analytics, location analysis, and mapping workflows.
  - Includes geocoding logic and location data export steps.
- zomato_part2.ipynb
  - Feature engineering and modeling preparation.
  - Includes label encoding, correlation analysis, and classifier setup.
- geocoding.ipynb
  - Focused notebook for geocoding address data.
- zomato_backup.ipynb
  - Extended backup version containing additional exploratory and mapping experiments.

## Python Packages Used

This project uses multiple Python libraries commonly used in data analysis and geospatial workflows:

- Data handling: pandas, numpy
- Visualization: matplotlib, seaborn, plotly, squarify
- Geospatial mapping: folium, folium.plugins (HeatMap, FastMarkerCluster)
- Geocoding: geopy (Nominatim, timeout handling)
- Machine learning: scikit-learn
  - LabelEncoder
  - RandomForestClassifier
  - train_test_split
  - TfidfVectorizer
  - TSNE

## Geocoding Contribution

Geocoding was a major custom step in this project and was done manually by me to obtain restaurant coordinates.

What was done:

- Extracted and cleaned address-level records.
- Geocoded addresses using geopy + Nominatim.
- Managed null/missing or timeout-prone results during lookup.
- Stored final latitude/longitude outputs in addresses_with_coordinates.csv.
- Used the coordinates for map visualizations and location insights.

## Key Results and Visual Outputs

### 1) Bubble Map

Restaurant distribution and intensity by location.

![Bubble Map](bubble_map.png)

### 2) Cluster Plot on Map

Spatial grouping pattern of restaurants across Bangalore.

![Cluster Plot](cluster_plot.png)

### 3) Heatmap

High-density restaurant activity zones.

![Heatmap](heatmap.png)

### 4) Scatter Plot on Map

Point-based spatial spread and concentration.

![Scatter Plot on Map](scatter_plot_on_map.png)

### Interactive output

- bubble_map.html provides an interactive map view.

## Typical Workflow

1. Load raw data from zomato.csv.
2. Clean and prepare address/location-level subsets.
3. Geocode address records to generate latitude/longitude.
4. Build map-based spatial visualizations.
5. Run EDA and feature analysis.
6. Encode features and prepare ML-ready data in df_le.csv.

## How to Run

1. Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn plotly folium geopy scikit-learn squarify jupyter
```

2. Open notebooks in Jupyter:

```bash
jupyter notebook
```

3. Run in recommended order:

- zomato_part1.ipynb
- geocoding.ipynb
- zomato_part2.ipynb

## Project Outcome

This project demonstrates practical data analyst skills across:

- Data cleaning and transformation
- Visual storytelling and dashboard-style plotting
- Geospatial enrichment through geocoding
- Spatial analysis and map-based insights
- ML preprocessing and feature engineering

It is a complete analyst portfolio-style case showing how raw restaurant data can be transformed into business and location intelligence.