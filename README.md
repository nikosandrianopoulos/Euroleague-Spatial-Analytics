# Euroleague Spatial Analytics & Performance Dashboard

## 📌 Project Overview
An end-to-end data analytics and spatial transformation tool that processes official **Euroleague post-game tracking datasets**. This project extracts raw event telemetry via API endpoints, calibrates spatial shot coordinates to standard FIBA regulations, and dynamically evaluates player offensive efficiency using advanced data science metrics.

Built entirely as a **generic, reusable template**, this framework can ingest any Euroleague Game ID or Player Name without requiring manual structural code modifications.

---

## 🛠️ Key Technical Features
* **Data Extraction & Ingestion:** Connects to official post-game endpoints to parse match event tracking layers.
* **Spatial Optimization ($Y-80$ Offset Calibration):** Features a vectorized data transformation pipeline to normalize coordinate telemetry, aligning raw tracking points perfectly with FIBA visual court dimensions.
* **High-Performance Computation:** Optimized via one-pass dictionary aggregations (`.value_counts().to_dict()`) rather than heavy iterative Pandas loops, drastically minimizing execution time.
* **Statistical Profiling:** Generates dynamic spatial Shot Charts and continuous distance distributions (Violin Plots) utilizing Seaborn and Matplotlib.

---

## 📊 Core Metrics & Analytical Glossary
To evaluate true scoring efficiency without volume bias, the script automates the calculation of industry-standard advanced basketball metrics:

* **Effective Field Goal Percentage (eFG%):** Adjusts traditional shooting metrics by giving appropriate weight to the extra value of 3-point field goals.
* **True Shooting Percentage (TS%):** The ultimate measure of shooting efficiency, accounting for Field Goals and Free Throws ($FTA$) weighted by an industry-standard possession coefficient ($0.44$).

---

## 💻 Tech Stack
* **Language:** Python 3.9
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Seaborn, Matplotlib
* **Environment:** Jupyter Notebook

---
---

## 📈 Sample Terminal Output
When executed, the script yields an **Ultimate Analytics Report** alongside visual dashboards
