<div align="center">

# 📊 Meta Ad Performance Dashboard

## End-to-End Business Intelligence & Marketing Analytics Project

**Transforming 400,000+ multi-platform advertising event interactions into actionable marketing insights using Power BI, Power Query, Star Schema Data Modeling & DAX**

![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Power Query](https://img.shields.io/badge/Power_Query-ETL-0F9D58?style=for-the-badge)
![DAX](https://img.shields.io/badge/DAX-Calculations-6A1B9A?style=for-the-badge)
![Data Modeling](https://img.shields.io/badge/Data_Modeling-Star_Schema-1E88E5?style=for-the-badge)
![Digital Marketing](https://img.shields.io/badge/Domain-Performance_Marketing-0081FB?style=for-the-badge&logo=meta&logoColor=white)

</div>

> **Note:** This project is built using a comprehensive Meta advertising performance dataset representing real-world digital marketing campaigns across Facebook and Instagram from **7 May 2025 to 6 August 2025**.

---

# 📊 Project Overview

This project presents an end-to-end Business Intelligence solution developed to evaluate, analyze, and optimize digital ad performance across Meta platforms (**Facebook & Instagram**).

The project covers the entire data lifecycle: from raw multi-table ingestion and Power Query ETL transformations to building an optimized dimensional Star Schema, calculating advanced DAX metrics, implementing dynamic measure selectors, and designing an interactive dual-view executive dashboard.

The dashboard delivers granular visibility into ad reach, funnel conversion drop-offs, demographic engagement patterns, ad creative effectiveness, and campaign budget utilization across 400,000 tracked interaction events.

---

# 💼 Business Problem

Modern digital marketing teams manage substantial paid media budgets across fragmented platforms and creative formats. Without granular performance visibility:
- Ad budgets are frequently exhausted on underperforming creatives and low-intent audience segments.
- Teams struggle to isolate top-of-funnel reach efficiency (CTR) from bottom-of-funnel purchase conversions (CR).
- Media buyers lack clear visibility into peak user engagement hours, leading to sub-optimal ad delivery scheduling and high ad fatigue.

This project delivers a centralized Business Intelligence solution to monitor volume metrics, conversion efficiency, creative fatigue, and audience behavior across **50 campaigns, 200 distinct ads, and 9,841 unique targeted users**.

---

# 🎯 Project Objectives

- Design an end-to-end Marketing Business Intelligence workflow in Power BI.
- Clean, profile, and transform multi-table transactional event logs using Power Query.
- Architect an optimized Star Schema data model for scalable analytical reporting.
- Formulate standardized DAX KPIs including CTR, Engagement Rate, Conversion Rate, and Purchase Rate.
- Implement **Dynamic Measure Selection** via DAX parameters to allow cross-visual metric exploration without visual clutter.
- Develop dedicated interactive dashboards for **Facebook** and **Instagram** performance.
- Extract data-backed recommendations to optimize paid ad spend and dayparting strategies.

---

# ⭐ Project Highlights

- Multi-Table Relational Architecture (Fact & Dimension Tables)
- Comprehensive Power Query Data Cleaning & Type Formatting
- Star Schema Dimensional Modeling
- Advanced DAX Ratios & Disconnected Slicer Parameters
- Dynamic Visual Titles & Automated Format Switching
- Granular Funnel Diagnostics (Impressions ➔ Clicks ➔ Engagements ➔ Purchases)
- Time-Intelligence Trends (Monthly, Weekly, and Hourly Dayparting Curves)
- Demographic & Geographic Segmentation (Age, Gender, Country)

---

# 🛠️️ Technology Stack

| Category | Technology |
|---|---|
| **Business Intelligence** | Microsoft Power BI Desktop |
| **ETL & Data Cleaning** | Power Query (M Language) |
| **Data Modeling** | Star Schema (1:N Single-Direction Relationships) |
| **Analytical Calculations** | Advanced DAX (Data Analysis Expressions) |
| **Data Sources** | Relational CSV Event Logs (400,000 Records) |

---

# 📂 Dataset Overview

The project utilizes a structured relational marketing dataset capturing user-level ad interactions and campaign metadata.

## Coverage Summary

| Attribute | Details |
|---|---|
| **Dataset Type** | Paid Advertising Interaction Event Logs |
| **Time Period** | 7 May 2025 – 6 August 2025 (Active 4 Months) |
| **Platforms Covered** | Facebook & Instagram |
| **Creative Formats** | Carousel, Image, Stories, Video |
| **Total Tracked Budget** | $2,535,923.78 (~$2.5M) |

## Dataset Statistics

| Dataset Table | Role | Records | Description |
|---|---|---:|---|
| **`ad_events`** | Fact Table | 400,000 | Granular events (Impressions, Clicks, Likes, Comments, Shares, Purchases) |
| **`campaigns`** | Dimension Table | 50 | Campaign metadata, start/end dates, duration, and allocated budgets |
| **`ads`** | Dimension Table | 200 | Creative ID, platform, ad type, and demographic targeting rules |
| **`users`** | Dimension Table | 9,841 | User demographic profiles, age, gender, country, and interest tags |

---

# 🔄 End-to-End Workflow

```text
Raw Marketing CSV Datasets (4 Tables)
                │
                ▼
Power Query ETL (Data Cleaning, Types, Handling Blanks)
                │
                ▼
Star Schema Data Model (1:N Relational Integrity)
                │
                ▼
DAX Measure Engineering & Dynamic Slicers
                │
                ▼
Interactive Multi-Page Power BI Dashboard
                │
                ▼
Executive Insights & Media Spend Recommendations
