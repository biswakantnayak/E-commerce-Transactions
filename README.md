# Online Retail Dataset – Analysis & Insights

## Project Overview

This project analyzes the **Online Retail Dataset (Dec 2010 – Dec 2011)** to uncover **sales trends, customer behavior, product performance, and profitability insights**. The goal is to leverage data cleaning, EDA, feature engineering, and forecasting to provide actionable business recommendations.

---

## Dataset Summary

* **Title:** Online Retail Dataset (E-commerce Transactions)
* **Source:** Public E-commerce transaction data
* **Domain:** Retail Analytics / E-commerce
* **Time Period:** Dec 2010 – Dec 2011
* **Shape (raw):** 541,909 rows × 8 columns
* **Final Shape (cleaned):** 461,180 rows × 8 columns

**Columns:**

* `InvoiceNo` – Unique transaction ID
* `StockCode` – Product code
* `Description` – Product description
* `Quantity` – Units purchased
* `InvoiceDate` – Date & time of purchase
* `UnitPrice` – Price per unit
* `CustomerID` – Unique customer ID
* `Country` – Country of transaction

---

## 🛠️ Data Preprocessing

* Removed **negative values** (cancelled orders/adjustments).
* Handled **missing values** in `CustomerID` & `Description`.
* Removed **5,268 duplicate records**.
* Detected & handled **outliers** in `Quantity` and `UnitPrice`.
* Final dataset reduced to **461,180 rows**.

---

## Exploratory Data Analysis (EDA)

* **Top Countries:** UK dominates sales, followed by Germany, France, EIRE & Netherlands.
* **Monthly Trends:** Strong **seasonality** – peak sales in Nov & Dec (holiday season).
* **Products:** Few products generate majority of revenue.
* **Customer Behavior:** Revenue concentrated in a few regions; repeat purchases are key.
* **Correlations:** `InvoiceNo` & `InvoiceDate` strongly correlated; weak link between `InvoiceDate` & `CustomerID`.

---

## Feature Engineering

* `Total_Sales` = Quantity × UnitPrice
* `Year`, `Month` from InvoiceDate
* `CostPrice` (assumed = 70% of UnitPrice)
* `Profit` = (UnitPrice – CostPrice) × Quantity
* `Profit Margin` = Profit ÷ Total\_Sales

---

## Model Building

* **Forecasting:** Applied **RandomForestRegressor** to predict monthly sales for 2012.
* **Result:** Increasing trend in early months, peak during holiday season (similar to 2011).

---

## Results & Visualizations

* **Total Sales:** 5,398,658.42
* **Total Quantity Sold:** 2,849,847 units
* **Unique Products:** 3,831
* **Highest Sales:** November & December

*Visualized sales, profit, quantity, and profit margins with bar & line plots.*

---

## Key Insights

*  **Seasonality:** Holiday season drives maximum sales.
*  **Geography:** UK is the primary revenue driver.
*  **Product Mix:** Few products dominate sales & profits.
*  **Profit Margins:** Wide variation across products.

---

## Recommendations

1. **Inventory Planning:** Stock up before holiday season.
2. **Geographic Expansion:** Target non-UK markets.
3. **Product Strategy:** Focus on high-margin products & bundles.
4. **Customer Retention:** Loyalty programs & discounts for repeat buyers.
5. **Forecast Usage:** Optimize supply chain & staffing during peak months.

---

## Conclusion

The Online Retail dataset highlights strong **seasonality, geographic concentration, and profit variation across products**. By optimizing product mix, expanding to new markets, and leveraging forecasting, businesses can **maximize sales and profitability**.

---
