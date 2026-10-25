# Real-Time Inventory & Demand Forecasting Engine

An interactive, web-based dashboard built with **React**, **Tailwind CSS**, and **Chart.js** that helps businesses monitor stock levels in real time and predict future product demand using mathematical forecasting models.

---

## What Does This Project Do?

Managing stock for a store or warehouse is tricky:
* If you **run out of stock**, you lose customers and money.
* If you **buy too much stock**, your cash gets trapped in items sitting on shelves.

This project solves that problem by giving store managers two simple tools:

1. **Live Stock Tracker:** Shows all products, their current stock levels, and automatically alerts you with a **"Reorder Needed"** warning whenever stock drops below a safe limit.
2. **Demand Forecasting Engine:** Takes past sales history and uses mathematical formulas to predict how many units customers will buy in the coming days.

---

## How the Forecasting Math Works

Instead of guessing future sales, this app uses two standard mathematical methods:

### 1. Simple Moving Average (SMA)
* **How it works:** It takes the average sales over the last $k$ days (for example, the last 3 days) to predict tomorrow's sales.
* **Best used for:** Products with steady, predictable sales that don't change drastically from day to day.

### 2. Single Exponential Smoothing (SES)
* **How it works:** It looks at past sales but gives **more weight to recent days**. 
* **The alpha Slider:** You can adjust the sensitivity slider ($\alpha$ between 0.1 and 0.9):
  * **Higher alpha (e.g., 0.8):** The prediction reacts quickly to sudden spikes or drops in recent sales.
  * **Lower alpha (e.g., 0.2):** The prediction smoothes out short-term fluctuations to show the broader long-term trend.
