# 📦 Data-Driven Inventory Optimization using ABC & Demand Variability Analysis

### 👤 Abdul Hadi

**Roll No:** 22f1001445
**Program:** IITM BS Degree

---

## 📌 Project Overview

This project develops a **data-driven inventory optimization framework** for a small-scale furniture component supplier using real transaction data (April–July 2025).

The business operates in:

* Furniture frames (raw & polished)
* Timber (e.g., teak sawn timber)
* Structural components

The existing system relied on **manual inventory tracking**, resulting in poor visibility, inefficient stocking, and capital blockage.

---

## 🎯 Objective

To design a **quantitative inventory management system** that:

* Identifies high-impact SKUs
* Incorporates demand variability into decisions
* Optimizes safety stock levels
* Improves reorder policies
* Reduces excess inventory holding

---

## ⚠️ Problem Statement

Key operational challenges:

* ❌ No structured SKU prioritization
* ❌ High variability in demand across products
* ❌ Excess inventory due to safety buffers
* ❌ Capital locked in low-performing SKUs
* ❌ Lack of data-driven replenishment policy

---

## 🧠 Analytical Framework

The project follows a structured pipeline:

1. **Data Collection & Preparation**

   * SKU-level sales and purchase data
   * Cleaning and aggregation

2. **Traditional ABC Analysis**

   * Based on profit contribution
   * Classification:

     * Top 70% → Class A
     * Next 20% → Class B
     * Remaining → Class C

3. **Multi-Criteria ABC Classification**

   * Composite score based on:

     * Profit (40%)
     * Sales Frequency (30%)
     * Demand Stability (30%)

4. **Demand Variability Analysis**

   * Measured using **Coefficient of Variation (CV)**
   * Identifies stable vs volatile SKUs

5. **Inventory Modeling**

   * Safety stock calculation using service levels
   * Reorder level estimation

---

# 📊 Visual Analysis

---

## 🔹 Multi-Criteria ABC Classification

![Multi ABC](assets/graphs/ABC.png)

📌 Insights:

* SKUs are ranked using a **composite performance score**
* Stable, high-frequency products move to higher priority
* High-variability SKUs are penalized

👉 **Improvement over traditional ABC:**
Accounts for operational reliability, not just profit.

---

## 🔹 Profit Distribution by ABC Category

![Profit Distribution](assets/graphs/ProfitDistribution.png)

📌 Insights:

* Class A contributes **~78% of total profit**
* Strong evidence of **Pareto Principle (80/20 rule)**
* Class B and C have significantly lower financial impact

👉 **Business implication:**
Focus should be on optimizing Class A inventory policies.

---

## 🔹 Reorder Level & Safety Stock Composition

![Reorder Level](assets/graphs/ReorderLevel.png)

📌 Insights:

* Safety stock forms **major portion of inventory (60–75%)**
* High demand variability significantly increases stock levels
* Example: Teak Sawn Timber shows excessive buffer stock

👉 **Critical finding:**
Inventory cost is driven more by **uncertainty than demand volume**

---

## 📈 Key Findings

### 1. Profit Concentration

* Small number of SKUs dominate revenue
* However, profit alone is insufficient for decision-making

---

### 2. Multi-Criteria Model Effectiveness

* Better prioritization of SKUs
* Stable products are correctly promoted
* Risky (high variability) products are downgraded

---

### 3. Demand Variability as Core Driver

* High CV → high safety stock
* Leads to overstocking and capital inefficiency

---

### 4. Inventory Inefficiency Root Cause

> Inventory risk is driven primarily by **demand variability rather than demand volume**

---

## 🔁 Inventory Model

Reorder Level:

```
Reorder Level = Demand during Lead Time + Safety Stock
```

Where:

* Safety Stock = Z × σ × √(Lead Time)
* Z depends on service level

Service Levels Used:

* Class A → Z = 1.88
* Class B → Z = 1.65
* Class C → Z = 1.28

---

## 🧠 Recommendations

### 🔄 Inventory Policy

* **Continuous Review System** → Class A (high priority)
* **Periodic Review System** → Class B & C

---

### 📉 Stock Optimization

* Reduce safety stock for declining-demand SKUs
* Avoid overstocking volatile products

---

### ⚖️ Strategic Actions

* Implement SKU-wise inventory planning
* Use variability-based decision-making
* Improve demand tracking mechanisms

---

## 🚀 Future Scope

* 📊 Demand Forecasting (ARIMA / Machine Learning)
* 📈 Real-time inventory dashboard (Power BI / Streamlit)
* 🔄 Automated inventory tracking system
* 🧠 Advanced optimization models (EOQ, stochastic models)
* 📦 Multi-location inventory management

---

## 📁 Repository Structure

```
project-root/
│── assets/
│    └── graphs/
│         ├── ABC.png
│         ├── ProfitDistribution.png
│         └── ReorderLevel.png
│── data/
│── README.md
```

---

## 📌 Key Takeaway

This project demonstrates that:

> Combining **multi-criteria classification + demand variability analysis** enables more accurate, efficient, and practical inventory decisions in real-world supply chains.

---

## 💼 Resume Highlight

* Developed a data-driven inventory optimization model using multi-criteria ABC classification and demand variability analysis, improving SKU prioritization and reducing excess safety stock impact.
