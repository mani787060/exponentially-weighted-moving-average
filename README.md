# Climate Trend Analysis using Exponentially Weighted Moving Average (EWMA)

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Domain](https://img.shields.io/badge/Domain-Time%20Series%20Analysis-green)
![Technique](https://img.shields.io/badge/Technique-EWMA-orange)
![Environment](https://img.shields.io/badge/Environment-Jupyter%20Notebook-orange)

## Project Overview

Time-series data often contains short-term fluctuations that make it difficult to identify underlying trends. Daily weather measurements, for example, can change because of local weather conditions and other temporary factors.

This project demonstrates **Exponentially Weighted Moving Average (EWMA)** using the Daily Delhi Climate dataset.

EWMA is a time-series smoothing technique that assigns greater importance to recent observations while gradually reducing the influence of older observations.

The project explores how exponential smoothing can help visualize climate-related trends in variables such as mean temperature, humidity, and wind speed.

The primary objective is to understand the mathematics behind EWMA, explore the effect of its smoothing parameter, and apply the technique to real-world climate data using Python.

## Project Objectives

- Understand the concept and mathematical foundation of EWMA.
- Learn how recent observations receive greater weights than older observations.
- Apply exponential smoothing to real-world climate data.
- Explore how changing the smoothing parameter affects the resulting trend.
- Compare original time-series observations with their smoothed values.
- Develop practical knowledge of time-series analysis using Pandas and Python.

## Dataset

This project uses the **Daily Delhi Climate Test Dataset**.

Dataset file: `DailyDelhiClimateTest.csv`

The dataset contains daily climate observations with the following columns:

| Column | Description |
|---|---|
| `date` | Date of the climate observation |
| `meantemp` | Mean temperature recorded for the day |
| `humidity` | Humidity measurement |
| `wind_speed` | Wind speed measurement |
| `meanpressure` | Mean atmospheric pressure |

These variables provide an opportunity to explore how EWMA can smooth fluctuations in different climate measurements.

**Dataset source:** [Daily Climate Time Series Data – Kaggle](https://www.kaggle.com/datasets/sumanthvrao/daily-climate-time-series-data)

## Understanding EWMA

### 1. What is Exponentially Weighted Moving Average?

EWMA is a smoothing method used to calculate a weighted average of time-series observations.

Unlike a Simple Moving Average (SMA), which assigns equal weights to observations within a fixed window, EWMA gives more importance to recent observations.

As observations become older, their influence decreases exponentially.

### 2. Mathematical Formula

The EWMA calculation can be expressed as:

\[
EWMA_t = \beta EWMA_{t-1} + (1-\beta)X_t
\]

Where:

- \(EWMA_t\): Current exponentially weighted average.
- \(EWMA_{t-1}\): Previous exponentially weighted average.
- \(X_t\): Current observation.
- \(\beta\): Smoothing or decay parameter.

The value of \(\beta\) controls how quickly older observations lose their influence.

### 3. Understanding the Smoothing Parameter

The smoothing parameter determines how responsive the EWMA curve is to changes in the original data.

- **Higher beta:** Gives more weight to the previous smoothed value, producing a smoother curve that reacts more slowly to recent changes.
- **Lower beta:** Gives more weight to the current observation, producing a more responsive curve that follows recent fluctuations more closely.

Therefore, selecting an appropriate smoothing parameter depends on the characteristics of the time series and the objective of the analysis.

### 4. EWMA vs Simple Moving Average

| Feature | Simple Moving Average | EWMA |
|---|---|---|
| Weight assignment | Equal weights within a window | Exponentially decreasing weights |
| Recent observations | Same weight as other window observations | Greater weight |
| Older observations | Removed after leaving the window | Influence gradually decreases |
| Main parameter | Window size | Smoothing parameter |
| Responsiveness | Depends on window size | Depends on smoothing parameter |

## Project Implementation

The complete implementation is available in the Jupyter Notebook:

`exponentially-weighted-moving-average.ipynb`

The project focuses on the following areas:

### Step 1: Data Loading

Load the Daily Delhi Climate dataset using Pandas and inspect its structure.

### Step 2: Data Exploration

Explore the available climate variables and understand how their values change over time.

### Step 3: Applying EWMA

Apply exponential smoothing to selected climate measurements to calculate smoothed time-series values.

### Step 4: Parameter Exploration

Explore the effect of different smoothing parameter values and understand how they influence the responsiveness and smoothness of the EWMA curve.

### Step 5: Visualization

Visualize and compare the original observations with the smoothed values to understand how EWMA reduces short-term fluctuations.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data loading and time-series manipulation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Jupyter Notebook | Interactive development and experimentation |

## Repository Structure

```text
exponentially-weighted-moving-average/
│
├── DailyDelhiClimateTest.csv
├── exponentially-weighted-moving-average.ipynb
└── README.md
```

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/mani787060/exponentially-weighted-moving-average.git
```

### 2. Navigate to the Project Directory

```bash
cd exponentially-weighted-moving-average
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Run the Notebook

Open:

`exponentially-weighted-moving-average.ipynb`

Execute the notebook cells in sequence to explore the dataset and understand the application of EWMA.

Make sure `DailyDelhiClimateTest.csv` remains in the same directory as the notebook so that the dataset can be loaded correctly.

## Practical Applications of EWMA

EWMA is useful in several areas where recent observations should have greater influence on a running estimate.

Some examples include:

- **Financial Analysis:** Smoothing financial time series and tracking changing market indicators.
- **Climate Analysis:** Understanding smoothed patterns in daily temperature, humidity, and other weather measurements.
- **Signal Processing:** Reducing short-term fluctuations in noisy signals.
- **Quality Control:** Monitoring process measurements and identifying unusual changes.
- **Machine Learning Optimization:** Understanding moving averages used in optimization algorithms such as momentum-based gradient descent and Adam.

## Key Learnings

Through this project, I explored:

- The mathematical foundation of exponentially weighted averages.
- The difference between EWMA and Simple Moving Average.
- How the smoothing parameter controls responsiveness.
- How to apply exponential smoothing to real-world time-series data.
- How Pandas can be used for time-series manipulation.
- How visualization helps interpret noisy data and smoothed trends.
- The broader connection between moving averages and machine learning optimization.

## Future Improvements

Some possible extensions of this project include:

- Comparing EWMA with Simple Moving Average and other smoothing techniques.
- Experimenting with additional smoothing parameter values.
- Evaluating smoothing performance using different time-series datasets.
- Exploring EWMA-based anomaly detection.
- Extending the analysis to forecasting methods.
- Studying the role of exponential moving averages in optimization algorithms such as Adam and RMSprop.

## Author

**Mani Ratan**

- GitHub: [@mani787060](https://github.com/mani787060)
- Repository: [Exponentially Weighted Moving Average](https://github.com/mani787060/exponentially-weighted-moving-average)

---

*This project is part of my continuous learning journey in Data Science, Machine Learning, and time-series analysis.*
