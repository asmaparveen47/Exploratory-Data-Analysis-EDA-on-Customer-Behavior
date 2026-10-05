
# Customer Metrics EDA & Revenue Drivers

An end-to-end data analytics project focused on preprocessing raw transactional records, performing Exploratory Data Analysis (EDA), and uncovering consumer spending insights.

## 📌 Project Overview
This project delivers a targeted **Ad Hoc Analysis** on a retail dataset containing **over 10,000 rows** of transaction history. By clearing type mismatches and missing values, this study outlines core audience profiles, maps regional footprints, and identifies a critical **loyalty paradox** where customer tenure does not automatically drive higher transaction sizes.

## 🏗️ Project Architecture & Data Pipeline
[Raw Data] ➔ [Data Cleaning Layer] ➔ [Feature Engineering] ➔ [EDA & Heatmaps] ➔ [Business Strategy]

* **1. Data Ingestion:** Sets up the Python runtime environment utilizing `Pandas` for structural manipulation, `Matplotlib` for basic charting, and `Seaborn` for correlation grids.
* **2. Data Cleaning Layer:** Resolves memory overhead and structural warnings using `.copy()`. Converts text fields (`Age`, `Purchase_Amount`, `Feedback_Score`) into floating-point numbers (`float`) and text strings into calendar timestamps (`datetime64[ns]`).
* **3. Feature Engineering:** Creates customized categorical buckets for customer lifetime (`Time_Range`) and age brackets (`Age_Group`) spanning children up to seniors. Synthetically calculates operational loyalty tenure (`Days_Active`).
* **4. Visual Analytics Engine:** Computes value frequencies (`value_counts()`) and linear relationship arrays via Pearson's correlation, rendering data via bounding-locked matrices and frequency distribution bar charts.

## 📊 Key Analytical Insights

### ⚡ The Loyalty Paradox
* While customer retention is phenomenal—the absolute majority of users remain active for **2+ years**—the calculated correlation between customer active days and spending size is effectively zero (**0.01**).

<img width="795" height="643" alt="Screenshot 2026-10-05 170647" src="https://github.com/user-attachments/assets/39a9f8c6-c69d-4abc-a0df-e3de1a61465b" />

* **Business Takeaway:** Customer lifetime length does *not* automatically scale your revenue metrics. Long-term loyalists purchase identical basket sizes compared to brand-new accounts.

### 🌐 Market Independent Traits
* Customer age and feedback scores operate completely independently of overall spending levels (Correlation scores hover between `-0.009` and `0.015`).
* Happier customer review scores do not organically convert into larger transaction sizes.

### 🗺️ Geographic & Demographic Core
* **Regional Hub:** **Kolkata completely dominates the footprint** with **2,255 customers**, while all other core cities (Mumbai, Bangalore, Chennai, Delhi, Hyderabad) split perfectly evenly at roughly ~1,350 users each.
* **Audience Profile:** The platform footprint heavily targets **Middle-Aged adults (4,058)** and leans significantly toward **Male users (4,958)**.

## 💡 Strategic Action Plan

* **VIP Incentive Milestones:** Launch tiered reward metrics for 1 and 2-year users to drive up their average basket sizes over time.
* **Scale the Kolkata Model:** Replicate the marketing distribution channels used in Kolkata across lower-performing regions like Mumbai and Delhi to expand the customer footprint.
* **Capture Demographic Gaps:** Deploy targeted promotional campaigns to tap into lagging female consumer spaces and younger demographics.

