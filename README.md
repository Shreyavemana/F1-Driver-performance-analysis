# 🏎️ F1 Driver Performance Analysis & Ranking System

## 📌 Project Overview

This project presents an end-to-end **Data Science and Machine Learning analysis of Formula 1 driver performance** using historical race data.
The goal is to **quantitatively evaluate, compare, and rank F1 drivers** across seasons by engineering meaningful performance metrics and applying unsupervised learning techniques.

The analysis combines **exploratory data analysis, feature engineering, clustering, and dimensionality reduction** to uncover performance patterns, driver archetypes, and long-term trends in Formula 1.

---

## 📊 Dataset

* **Source:** Kaggle – Formula 1 Race Data (Ergast API dump)
* **Coverage:** 1950 – 2023
* **Key Tables Used:**

  * `races`
  * `results`
  * `drivers`
  * `constructors`
  * `qualifying`
  * `circuits`

This dataset provides comprehensive information about race outcomes, driver details, constructors, qualifying positions, and circuits.

---

## 🔧 Data Processing & Feature Engineering

The raw datasets are merged into a unified analytical table using race IDs, driver IDs, and constructor IDs.

Key preprocessing steps include:

* Handling missing and non-numeric race positions (DNFs, disqualifications)
* Creating a **DNF indicator**
* Calculating **qualifying vs race position delta**
* Restricting analysis to modern F1 seasons (2010 onwards) for relevance

---

## 📈 Driver Performance Metrics

For each **driver-season**, the following metrics are computed:

* Total races participated
* Total points scored
* Points per race
* Average finishing position
* Consistency score (inverse of position variance)
* DNF rate
* Average qualifying vs race performance delta

### 🏁 Custom Performance Score

A weighted composite score is designed to rank drivers:

* Points per race (performance output)
* Average finishing position (race quality)
* Consistency score (stability)
* Qualifying efficiency (race execution)

This score enables **objective driver ranking across seasons**.

---

## 🏆 Key Analyses Performed

### 1. **Top Drivers Per Season**

* Identifies the top-performing drivers for selected seasons
* Tracks performance evolution over time

### 2. **Constructor Dominance Analysis**

* Evaluates constructor influence on driver success
* Visualizes championship trends across seasons

### 3. **Track-wise Driver Performance**

* Analyzes how top drivers perform across different circuits
* Uses heatmaps to reveal track-specific strengths

### 4. **Driver Improvement Analysis**

* Measures year-over-year improvement and decline
* Highlights rising talents and performance drops

---

## 🤖 Machine Learning Components

### 🔹 K-Means Clustering

Drivers are clustered based on average performance characteristics:

* Points per race
* Consistency
* Average finishing position
* DNF rate
* Qualifying performance

This identifies **distinct driver archetypes**, such as:

* Elite consistent performers
* High-risk high-reward drivers
* Midfield steady drivers

Cluster quality is validated using **Silhouette Score** and the **Elbow Method**.

---

### 🔹 Principal Component Analysis (PCA)

* Reduces high-dimensional performance metrics into key latent dimensions
* Demonstrates that **2–3 components explain most performance variance**
* Visualizes drivers in a low-dimensional performance space

---

## 📊 Visualizations

The project includes rich, interactive visualizations:

* Time-series performance plots
* Constructor dominance trends
* Heatmaps of driver vs circuit performance
* PCA cluster projections
* Radar charts comparing top drivers across metrics

Libraries used:

* Matplotlib & Seaborn
* Plotly (interactive charts)

---

## 🎯 Key Insights

* Driver performance can be effectively captured using a small set of engineered metrics
* Consistency plays a critical role in championship success
* Constructor dominance significantly influences driver rankings
* Clustering reveals meaningful driver performance archetypes
* Qualifying performance has a strong correlation with race outcomes

---

## 🛠 Tech Stack

* **Python**
* **Pandas, NumPy**
* **Scikit-learn**
* **Matplotlib, Seaborn**
* **Plotly**
* **Google Colab**

---

## 🚀 How to Run

1. Open the notebook in **Google Colab**
2. Install required libraries (handled in the notebook)
3. Download dataset automatically via `kagglehub`
4. Run all cells sequentially to reproduce analysis and visualizations

---

## 📌 Future Improvements

* Incorporate lap-time and pit-stop data
* Add predictive modeling for race outcomes
* Deploy an interactive Streamlit dashboard
* Compare teammate performance within the same constructor

---

## 📜 License

This project is intended for **educational and analytical purposes only**.
Formula 1 data is sourced from publicly available datasets.


