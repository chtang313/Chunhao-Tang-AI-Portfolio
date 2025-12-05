# 🧭 Ground Team Retail Store Assignment

This project automates the preparation of retail location data so ground teams can be assigned to stores efficiently. The workflow cleans raw CSV files, removes duplicates, converts locations into KML for mapping in Google Earth, and prepares the data for clustering and territory planning.

---

## 📌 Project Overview

Real-world retail datasets often contain duplicates, inconsistent formatting, and missing fields. This project takes raw store CSV files for multiple cities, cleans and standardizes them, and outputs files that can be visualized on a map and used for proximity-based clustering and team assignment.

Key goals:

- Consolidate and clean retailer CSV files  
- Remove duplicate or invalid entries  
- Generate KML files that can be loaded directly into Google Earth  
- Prepare a clean dataset for geographic clustering and territory planning  

---

## 🧰 Technologies & Files

**Core tools**

- Python  
- Jupyter Notebook  

**Key libraries** (adjust to match your imports)

- `pandas` – data loading, cleaning, and transformation  
- `numpy` – numerical utilities  
- `geopandas` / `shapely` / `folium` (if used) – geospatial operations and visualization  
- Any KML-related library or manual export logic  

**Project files**

- `Cleanup-KML-and-Cluster-by-proximity.ipynb` – main pipeline notebook  
- `Zi-Dong-Hua-Qu-Yu-Zui-Zhong-Ban.ipynb` – additional automation / clustering experiments  
- `Greater-Houston-Retailers.csv` – raw Houston retailer data  
- `Greater-Houston-Retailers-Trimmed.csv` – cleaned Houston retailer data  
- `Dallas-Retailers.csv` – Dallas retailer data  

---

## 🔄 Data Pipeline

### 1️⃣ Ingest & Inspect

- Load raw CSV files for each region (e.g., Greater Houston and Dallas)  
- Inspect column names, missing values, and basic distributions  
- Standardize key fields such as store name, address, city, latitude, and longitude  

### 2️⃣ Clean & Deduplicate

- Remove exact and near-duplicate store records  
- Drop rows with missing or unusable location data  
- Normalize string fields (trimming whitespace, consistent casing)  
- Save the cleaned dataset (e.g., `Greater-Houston-Retailers-Trimmed.csv`)  

### 3️⃣ Export to KML for Google Earth

- Convert cleaned latitude/longitude data into a KML structure  
- Create placemarks for each retail location  
- Export the KML file and load it into **Google Earth** to verify locations on a map  

### 4️⃣ Cluster by Proximity (Assignment Prep)

- Use geographic distance or clustering logic (e.g., k-means or distance thresholds) to group nearby stores  
- Produce groupings that can be mapped to ground team routes or territories  
- Optionally export cluster assignments back into CSV for reporting and operations  

---

## 📊 Example Use Case

- A field operations manager needs to assign a limited number of ground team members to hundreds of retail stores across Greater Houston and Dallas.  
- This project provides a **clean, de-duplicated, mapped dataset** that can be clustered by proximity, making it easy to define routes or regions for each team member in minutes instead of manually planning from spreadsheets.  

---

## 📘 Learning Outcomes

By completing this project, you gain experience in:

- Cleaning and consolidating real-world retail store datasets  
- Removing duplicate location records and standardizing geospatial fields  
- Generating KML files for visualization in Google Earth  
- Using Python notebooks to build an end-to-end data pipeline from raw CSV to assignment-ready data  
- Laying the foundation for more advanced clustering and territory optimization models  

---

## ▶️ How to Run

1. Open `Cleanup-KML-and-Cluster-by-proximity.ipynb` in Jupyter or Google Colab.  
2. Ensure the CSV files (`Greater-Houston-Retailers.csv`, `Dallas-Retailers.csv`, etc.) are in the same directory or update the paths in the notebook.  
3. Install required libraries listed in the first notebook cell (e.g., `pip install pandas numpy` plus any geospatial/KML packages used).  
4. Run the notebook cells in order:
   - Data loading and inspection  
   - Cleaning and deduplication  
   - KML export  
   - Clustering / proximity-based grouping (if included)  
5. Open the generated KML file in **Google Earth** to view and verify store locations.

