# Exponentially Weighted Moving Average (EWMA)
[![ML Theory](https://img.shields.io/badge/Domain-Machine%20Learning%20Theory-blue)](https://en.wikipedia.org/wiki/Moving_average#Exponential_moving_average)
[![Mathematics](https://img.shields.io/badge/Focus-Time%20Series%20Analysis-orange)](https://www.investopedia.com/articles/06/ema.asp)
[![Optimization](https://img.shields.io/badge/Application-Deep%20Learning%20Optimizers-green)](https://distill.pub/2017/momentum/)

## 🏗️ Project Overview
This repository explores the mechanics of **Exponentially Weighted Moving Averages (EWMA)**. Unlike a Simple Moving Average (SMA) which weights all observations in a window equally, EWMA assigns weights that decrease exponentially as the data points get older. 

This project demonstrates how to "de-noise" volatile data to reveal underlying trends—a critical skill for time-series forecasting, financial modeling, and understanding the convergence of neural networks.

---

## 🛠️ Mathematical Foundations

### 1. The Recursive Formula
The EWMA at time $t$ is calculated using the recursive relationship:
$$v_t = \beta v_{t-1} + (1 - \beta) \theta_t$$
Where:
*   $v_t$: The current estimate (the "moving average").
*   $\beta$: The smoothing factor (typically between 0.9 and 0.99).
*   $\theta_t$: The current data point/observation.

### 2. The Power of "Memory"
The parameter **$\beta$** controls the model's memory:
*   **High $\beta$ (e.g., 0.98):** The model is "heavy" and slow to react; it averages over a larger window (approx. 50 days), creating a very smooth curve that is resistant to outliers.
*   **Low $\beta$ (e.g., 0.5):** The model is "light" and reactive; it behaves more like the original data, capturing rapid changes but including more noise.

---

## 🚀 Why This Matters for AI
This notebook isn't just about statistics—it is the blueprint for **Modern Optimization**:

1.  **Momentum:** Uses EWMA of gradients to help Gradient Descent "roll" over plateaus and damp out oscillations.
2.  **RMSProp:** Uses EWMA of squared gradients to normalize the learning rate.
3.  **Adam:** Combines both of the above. By mastering EWMA, you understand exactly how these optimizers compute their "moving averages" of historical updates to reach the global minimum faster.

---

## 💻 Tech Stack
*   **Language:** Python 3.9+
*   **Libraries:** NumPy, Pandas (for `.ewm()` comparisons), Matplotlib
*   **Environment:** Jupyter Notebook

---

## 📂 Usage
The implementation is detailed in `exponentially-weighted-moving-average.ipynb`. The notebook includes:
1.  Manual recursive implementation of the EWMA formula.
2.  Visual comparisons of different $\beta$ values on noisy synthetic data.
3.  Analysis of **Bias Correction**, explaining how to handle the initial steps where the average starts at zero.
