# Climate Trend Analysis using EWMA
[![Data Science](https://img.shields.io/badge/Domain-Climate%20Data%20Science-blue)](https://www.kaggle.com/datasets/sumanthvrao/daily-climate-time-series-data)
[![Method](https://img.shields.io/badge/Method-Exponential%20Moving%20Average-orange)](https://en.wikipedia.org/wiki/Moving_average#Exponential_moving_average)
[![Dataset](https://img.shields.io/badge/Dataset-Daily%20Delhi%20Climate-green)](./DailyDelhiClimateTest.csv)

## 🏗️ Project Overview
Weather data is inherently "noisy"—daily temperatures can fluctuate wildly due to localized events, making it difficult to see the bigger picture. This project utilizes the **Exponentially Weighted Moving Average (EWMA)** technique to process the **Daily Delhi Climate Dataset**. 

By applying exponential smoothing, we assign higher weights to recent observations while allowing the influence of older data to decay, effectively "filtering out" daily noise to visualize clean, seasonal climate transitions.

---

## 📊 Dataset & Implementation

### 1. The Daily Delhi Climate Data
The project utilizes `DailyDelhiClimateTest.csv`, focusing on key parameters:
*   **Mean Temperature:** Analyzing daily averages to find long-term heat patterns.
*   **Humidity:** Observing moisture trends across different months.
*   **Wind Speed:** Smoothing out gust data to find prevailing wind trends.

### 2. Weighted Smoothing Logic
Unlike a Simple Moving Average (SMA) which can be "laggy" and treats all days the same, the EWMA implementation here:
*   **Prioritizes Recency:** It reacts faster to genuine climate shifts (like the sudden onset of monsoon or heatwaves).
*   **Dynamic Windowing:** Demonstrates how adjusting the smoothing parameter ($\beta$) changes the "memory" of the model—from a 10-day trend to a 50-day seasonal outlook.

### 3. Visual Trend Extraction
The notebook provides high-quality visualizations comparing:
*   **Raw Data:** The "spiky" daily recorded values.
*   **EWMA Curve:** The smooth, mathematical trend line that highlights the actual climate trajectory.

---

## 💻 Tech Stack
*   **Language:** Python 3.9+
*   **Data Analysis:** Pandas, NumPy
*   **Visualization:** Matplotlib, Seaborn
*   **Environment:** Jupyter Notebook

---

## 🚀 Usage
The full analysis is contained in `exponentially-weighted-moving-average.ipynb`. 

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/climate-trend-analysis-ewma.git](https://github.com/your-username/climate-trend-analysis-ewma.git)

2. **Ensure the dataset is present:**

   Place DailyDelhiClimateTest.csv in the root directory.

3. **Run the Notebook:**
   Analyze how Delhi's climate patterns emerge once the daily noise is removed.   
