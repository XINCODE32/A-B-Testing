# 🧪 A/B Testing & Hypothesis Prioritization Project

## 📌 Project Overview

As an analyst at a large online store, you're working with the marketing team to boost revenue. This project focuses on **prioritizing marketing hypotheses** and **analyzing A/B test results** to determine which initiatives are most effective.

---

## 🗂️ Data Description

### 📁 Datasets

#### Part 1: Hypothesis Prioritization
- **`hypotheses_us.csv`**
  - `Hypothesis`: brief description of the idea
  - `Reach`: estimated number of users affected (1–10)
  - `Impact`: estimated effect on users (1–10)
  - `Confidence`: confidence level (1–10)
  - `Effort`: estimated resources needed (1–10)

#### Part 2: A/B Testing
- **`orders_us.csv`**
  - `transactionId`: unique order ID
  - `visitorId`: unique user ID
  - `date`: date of the order
  - `revenue`: revenue from the order
  - `group`: A/B test group (A or B)
  
- **`visits_us.csv`**
  - `date`: visit date
  - `group`: A/B group
  - `visits`: number of visits for the group on that day

---

## 🧪 Part 1: Hypothesis Prioritization

### ✅ Goals:
- Prioritize revenue-boosting hypotheses using:
  - **ICE** = (Impact × Confidence) / Effort
  - **RICE** = (Reach × Impact × Confidence) / Effort
- Rank hypotheses by each method
- Explain differences between ICE and RICE rankings

---

## 📊 Part 2: A/B Test Analysis

### 🔍 Key Tasks:

1. **Cumulative Revenue**
   - Compare total revenue by group over time

2. **Cumulative Average Order Size**
   - Compare average order value by group

3. **Relative Differences**
   - Measure daily and cumulative relative differences in order size between groups

4. **Conversion Rate Analysis**
   - Calculate daily conversion = orders / visits
   - Plot conversion rate by group

5. **User Behavior Analysis**
   - Scatter plot: number of orders per user
   - 95th & 99th percentiles to detect outliers (heavy users)

6. **Order Price Analysis**
   - Scatter plot of order values
   - Define abnormal orders based on 95th & 99th percentiles

7. **Statistical Significance**
   - Test difference in conversion between groups:
     - Using **raw data**
     - Using **filtered data** (after removing outliers)
   - Test difference in average order size between groups:
     - Raw vs. filtered data

8. **Decision-Making**
   - Based on analysis, choose one:
     - ✅ Stop the test and declare a winner
     - ❌ Stop the test, no difference
     - ⏳ Continue testing

---

## 📈 Tools & Libraries

- **Python**
  - `pandas`, `numpy` for data handling
  - `matplotlib`, `seaborn` for visualization
  - `scipy.stats` for statistical testing
- **Jupyter Notebook** for step-by-step EDA and analysis

---

## 🧠 Insights Expected

- Which marketing hypothesis has the most potential (based on ICE & RICE)?
- Does group B outperform group A in terms of:
  - Conversion rate?
  - Average order size?
  - Overall revenue?
- Are there anomalies (users or orders) skewing the data?
- What is the most data-driven decision to make from this test?
