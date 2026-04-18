# 🌍 EcoPredict: U.S. Air Quality Analysis & Forecasting

**EcoPredict** is an advanced Data Science project focused on analyzing and predicting atmospheric pollution levels across the United States. Utilizing high-resolution historical data from the **EPA (Environmental Protection Agency)**, this project employs Machine Learning to forecast the concentration of critical pollutants (NO₂, O₃, SO₂, and CO) and their impact on public health.

---

## 🔬 Project Overview

Air pollution is a global health crisis. In the U.S., despite strict regulations like the *Clean Air Act*, many urban and industrial hubs still face critical air quality challenges. 

This project aims to bridge the gap between raw environmental data and actionable insights by:
* **Trend Identification:** Decoding seasonal and decadal patterns in pollutant behavior.
* **Risk Mitigation:** Developing predictive models to serve as early warning systems for vulnerable populations.
* **Policy Support:** Providing data-driven evidence to aid environmental mitigation strategies.

---

## 📊 The Dataset

The analysis is powered by the **EPA Air Quality System (AQS)**.
* **Features:** Daily measurements of NO₂, O₃, SO₂, and CO concentrations.
* **Geography:** State-level and City-level granularity across the U.S.
* **Temporal Scope:** Historical records analyzed for long-term trend extraction.

> [!IMPORTANT]
> **Source:** Data retrieved from the [EPA Outdoor Air Quality Data portal](https://www.epa.gov/outdoor-air-quality-data).

---

## 🛠️ Technical Stack & Methodology

### **The Data Science Pipeline**
1. **EDA (Exploratory Data Analysis):** Deep dive into spatial-temporal distributions using `Seaborn` and `Matplotlib`.
2. **Preprocessing:** Handling missing values, outlier detection, and feature scaling.
3. **Feature Engineering:** Creating lag variables and rolling averages to capture temporal dependencies.
4. **Modeling:** Implementing a multi-model approach to find the best fit for time-series forecasting.

### **Technologies Used**
| Field | Tools |
| :--- | :--- |
| **Language** | Python 3.x |
| **Data Wrangling** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn, Plotly |
| **Machine Learning** | Scikit-learn, XGBoost, LightGBM |
| **Deep Learning** | TensorFlow / Keras (Experimental) |

---

## 📦 Custom Feature: Advanced Outlier Management

During the development phase, the high variance in sensor data presented a significant challenge. To solve this, I developed a **custom outlier detection and treatment module**. 

Environmental data often contains "spikes" that are not errors but critical events (wildfires, industrial leaks). My custom logic allows the model to:
* **Distinguish Noise from Events:** Filter out sensor malfunctions while preserving vital extreme-event data.
* **Improve Robustness:** Increase the R² score by reducing the impact of non-representative data points.
* **Automated Cleaning:** A modular approach that can be reused in other environmental time-series projects.

---

## ✅ Project Milestones & Results

- [x] **Data Ingestion:** Successful cleaning and normalization of massive EPA datasets.
- [x] **Statistical Hotspots:** Precise identification of the highest pollution zones in the U.S.
- [x] **Optimized Predictive Engine:** Finalized **XGBoost/LightGBM** models with hyperparameter tuning.
- [x] **Custom Tooling:** Successfully integrated the Outlier Analysis package into the main pipeline.

---
## 📊 Final Performance & Insights

* **Top Model:** XGBoost Regressor achieved the highest accuracy for NO₂ and O₃ levels.
* **Validation:** Models were validated using **RMSE** and **MAE** metrics to ensure reliable real-world performance.
* **Key Discovery:** Seasonal patterns and industrial density were identified as the primary drivers for NO₂ spikes.
