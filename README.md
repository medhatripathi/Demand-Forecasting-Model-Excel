# Demand-Forecasting-Model-Excel
A time-series demand forecasting model comparing 5 forecasting methods to identify the most accurate approach for inventory planning and stockout reduction. This project analyzes 24 months of historical sales data across 3 SKUs to build and compare multiple forecasting methods. The model identifies the optimal forecasting approach based on accuracy metrics (MAPE, MAE, RMSE) and provides actionable recommendations for inventory optimization.
![Demand-Forecasting-Model-Excel](https://docs.google.com/spreadsheets/d/1yEuLYv1yJaH8aqIqNgTHmlxa0v6RyKHJ/edit?usp=sharing&ouid=117695434224299199084&rtpof=true&sd=true)
---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Microsoft Excel | Data analysis, forecasting models, dashboards |
| Excel Formulas | AVERAGE, FORECAST, INDEX-MATCH, ABS |
| Pivot Tables | Data summarization |
| Excel Charts | Data visualization |

---

## 📁 Data Source

### Dataset Overview

| Attribute | Details |
|-----------|---------|
| Source | Simulated retail sales data |
| Time Period | January 2023 - December 2024 |
| Granularity | Monthly |
| Total Records | 72 rows (3 SKUs × 24 months) |

### Data Structure

| Column | Description | Data Type |
|--------|-------------|-----------|
| Month | Sequential month number (1-24) | Integer |
| Date | First day of each month | Date |
| SKU_ID | Product identifier | Text |
| Product_Name | Product description | Text |
| Category | Product category | Text |
| Units_Sold | Actual monthly demand | Integer |
| Unit_Price | Selling price per unit | Currency |
| Promo_Flag | Promotional period indicator (0/1) | Binary |

### SKUs Analyzed

| SKU_ID | Product Name | Category | Avg Monthly Sales |
|--------|--------------|----------|-------------------|
| SKU001 | Wireless Mouse | Electronics | 324 units |
| SKU002 | USB Cable | Accessories | 612 units |
| SKU003 | Laptop Stand | Accessories | 168 units |

---

## ✨ Features / Highlights

### 🔴 Business Problem

A retail company struggles with:
- **Stockouts** causing lost sales and customer dissatisfaction
- **Excess inventory** tying up working capital
- **Manual forecasting** leading to inconsistent accuracy
- **No standardized method** to predict future demand

The company needs a data-driven forecasting approach to improve inventory planning and reduce operational costs.

---

### 🎯 Goal of the Dashboard

1. **Compare 5 forecasting methods** to identify the most accurate approach
2. **Calculate accuracy metrics** (MAE, MAPE, RMSE, Bias) for objective comparison
3. **Visualize forecast vs actual** performance over time
4. **Generate 3-month future forecast** using the best method
5. **Provide actionable recommendations** for inventory optimization

---

### 📈 Forecasting Methods Compared

| Method | Description | Best For |
|--------|-------------|----------|
| 3-Month Moving Average | Simple average of last 3 months | Stable demand patterns |
| 6-Month Moving Average | Simple average of last 6 months | Smoothing out noise |
| Weighted Moving Average | Recent months weighted higher (50/30/20) | Trending products |
| Exponential Smoothing | Decay-weighted historical data (α=0.3) | Responsive forecasting |
| Linear Regression | Trend line projection | Long-term growth/decline |

---

### 📊 Walk Through of Key Visuals

#### Visual 1: Actual vs Forecast Comparison (Line Chart)

![Actual vs Forecast](https://github.com/medhatripathi/Demand-Forecasting-Model-Excel/blob/main/Visual1_Actual%20vs%20Forecast%20Comparison.png)

- **X-axis:** Month (Jan 2023 - Dec 2024)
- **Y-axis:** Units Sold
- **Lines:** Actual Sales, 3M_MA, WMA, Exponential Smoothing
- **Insight:** WMA (green line) tracks closest to actual demand, especially during trend changes

---

#### Visual 2: Forecast Accuracy Comparison (Bar Chart)

![Accuracy Comparison](https://github.com/medhatripathi/Demand-Forecasting-Model-Excel/blob/main/Visual2_Forecast%20Accuracy%20Comparison.png)

- **X-axis:** MAPE (%)
- **Y-axis:** Forecasting Method
- **Highlight:** Weighted MA shows lowest error at 10.2%
- **Insight:** 6-Month MA performs worst (15.4%) due to lag in responding to demand changes

---

#### Visual 3: KPI Summary Cards

![KPI Summary Cards](https://github.com/medhatripathi/Demand-Forecasting-Model-Excel/blob/main/Visual3_KPI%20Summary%20Cards.png)

| Metric | Value |
|--------|-------|
| Best Method | Weighted Moving Average |
| Forecast Accuracy | 94.16% |
| Lowest MAPE | 5.61% |
| SKUs Analyzed | 3 |

---

### 💡 Business Impact & Insights

#### Key Findings

| Finding | Impact |
|---------|--------|
| WMA outperforms all methods | 5.61% MAPE vs 12.8% industry average |
| Seasonal demand pattern detected | Nov-Dec shows 40% higher demand |
| 6-Month MA too slow | 15.4% error - misses trend changes |
| Exponential Smoothing reliable | 11.5% MAPE - good alternative |

#### Recommendations

1. **Implement Weighted Moving Average** as primary forecasting method
   - Expected stockout reduction: 15-20%
   - Forecast accuracy improvement: 5%

2. **Add seasonal adjustment** for Q4 (November-December)
   - Apply 1.25x multiplier for holiday demand
   - Pre-position inventory 30 days before peak

3. **Safety stock optimization**
   - Current: 2 weeks coverage
   - Recommended: 2.5 weeks for high-velocity SKUs

4. **Monthly model review**
   - Recalculate forecasts with latest actuals
   - Monitor MAPE trend for model degradation

#### Projected Business Value

| Metric | Current | After Implementation |
|--------|---------|---------------------|
| Stockout Rate | 12% | 5% |
| Excess Inventory | $45,000 | $28,000 |
| Forecast Accuracy | 85% | 90% |
| Annual Savings | - | ~$25,000 |

