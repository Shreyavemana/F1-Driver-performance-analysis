# F1-Driver-performance-analysis

🏎️ F1 Driver Performance Analysis & Ranking System
📌 Project Overview

This project performs an end-to-end data science and machine learning analysis of Formula 1 driver performance using historical race data.
By combining feature engineering, statistical analysis, clustering, and dimensionality reduction, the system builds a custom driver ranking framework and identifies distinct driver performance archetypes across multiple seasons.

The analysis focuses on modern F1 seasons (2010 onwards) to ensure relevance and consistency.

📊 Dataset

Source: Ergast Formula 1 Dataset (via Kaggle)

Coverage: 1950–2023 (analysis focused on 2010–2023)

Data Used:

Race results

Drivers and constructors

Qualifying positions

Circuits and race metadata

🔧 Data Processing & Feature Engineering

Multiple relational datasets were merged to create a unified race-level table.
Key engineered features include:

Average finishing position

Points per race

Driver consistency (position variance)

DNF (Did Not Finish) rate

Qualifying vs race performance delta

Custom Performance Score using a weighted scoring formula

Drivers with insufficient race participation were filtered to maintain fairness and statistical reliability.

📈 Exploratory Data Analysis

The project includes extensive analysis and visualization of:

Top drivers per season (2015–2023)

Driver performance trends over time

Constructor dominance and championship impact

Circuit-wise driver performance using heatmaps

Year-over-year driver improvement and decline patterns

Interactive visualizations were built using Plotly, alongside Matplotlib and Seaborn for statistical plots.

🤖 Machine Learning Component
Driver Clustering

Algorithm: K-Means

Features: Points per race, average position, consistency score, DNF rate, qualifying performance, performance score

Optimization: Elbow method and Silhouette score

The clustering process identified distinct driver archetypes, such as:

Elite championship contenders

Consistent midfield performers

High-risk / high-variance drivers

Developing or declining drivers

🔬 Dimensionality Reduction (PCA)

Principal Component Analysis (PCA) was applied to:

Identify key performance dimensions

Reduce feature complexity

Visualize driver clusters in 2D space

Results show that 2–3 principal components explain most of the variance in driver performance.

📡 Advanced Visual Comparisons

Radar charts comparing top drivers across multiple performance metrics

PCA scatter plots highlighting cluster separation

Performance trend visualizations across seasons

🎯 Key Insights

Consistency plays a critical role in long-term success, not just peak race results

Constructor dominance significantly influences driver performance outcomes

Qualifying performance strongly correlates with race results

Driver performance patterns can be effectively represented using low-dimensional feature spaces

🛠️ Tech Stack

Python

Pandas, NumPy

Scikit-learn

Matplotlib, Seaborn

Plotly (Interactive Visualizations)

Google Colab

🚀 Future Improvements

Incorporate weather and safety car data

Add lap-level telemetry for advanced strategy analysis

Deploy an interactive Streamlit dashboard

Explore predictive modeling for race outcomes

📌 Why This Project Matters

This project demonstrates:

Real-world data handling and feature engineering

Analytical thinking and metric design

Practical application of machine learning (unsupervised learning & PCA)

Strong visualization and storytelling skills
