# 📊 Meta Ad Performance Dashboard (Power BI)

An interactive, end-to-end business intelligence dashboard built in Microsoft Power BI to evaluate and optimize Meta (Facebook & Instagram) paid advertising campaigns across 400,000+ ad event interactions.

---

## 📌 Executive Summary & Objective

Modern digital marketing teams manage large budgets across multi-channel platforms. Without granular performance visibility, ad spend is often wasted on low-converting audiences and suboptimal ad formats. 

### **Primary Objectives:**
- **Performance Evaluation:** Track macro advertising volume (**Impressions, Clicks, Engagements, Purchases**) across Facebook and Instagram.
- **Funnel Conversion Analysis:** Measure efficiency ratios (**CTR, Engagement Rate, Conversion Rate, Purchase Rate**) to detect funnel drop-offs.
- **Budget & Resource Optimization:** Analyze campaign budget distributions against acquisition performance to guide budget allocation.
- **Audience & Creative Diagnostics:** Uncover high-performing demographics, geographic regions, ad placements, and peak interaction times.

---

## 📸 Dashboard Previews

### 1. Facebook Performance View
![Facebook Dashboard](Images/dashboard_facebook.png)

### 2. Instagram Performance View
![Instagram Dashboard](Images/dashboard_instagram.png)

---

## 🛠️ Tech Stack & Skills Demonstrated

- **Business Intelligence:** Microsoft Power BI Desktop
- **ETL & Data Cleaning:** Power Query (M Language)
- **Data Modeling:** Star Schema (Fact & Dimension Tables, One-to-Many Relationships)
- **Analytics & Calculations:** Advanced DAX (Data Analysis Expressions, Field Parameters, Time-Intelligence)
- **Data Source:** Meta Ad Event Logs (CSV, May – August 2025)

---

## 🧱 Data Architecture & Modeling

The project follows an optimized **Star Schema** architecture centered around user-ad interaction events:

```
          [Dim_Campaigns]
                 │ (1:N)
          [Dim_Ads]
                 │ (1:N)
[Dim_Users] ─── (1:N) ─── [Fact_Ad_Events] ─── (N:1) ─── [Dim_Calendar]
```

### **Table Dictionary:**
1. **`ad_events` (Fact Table - 400,000 Rows):** Granular user interactions recording `event_id`, `ad_id`, `user_id`, `timestamp`, and `event_type` (`Impression`, `Click`, `Purchase`, `Comment`, `Share`, `Like`).
2. **`campaigns` (Dimension Table):** Contains `campaign_id`, `name`, `start_date`, `end_date`, `duration_days`, and `total_budget` ($2.5M total budget tracked).
3. **`ads` (Dimension Table):** Attributes for each creative including `ad_id`, `ad_platform` (*Facebook*, *Instagram*), `ad_type` (*Carousel*, *Image*, *Stories*, *Video*), and target demographics.
4. **`users` (Dimension Table):** Demographics including `user_id`, `user_age`, `age_group`, `user_gender`, `country`, and interests.
5. **`Calendar Table` & `Dynamic Measure Selector`:** Disconnected parameter and date dimension tables supporting dynamic slicers and continuous time series.

---

## 📐 Key DAX Measures & Formulas

### 1. Performance Ratio Measures
- **Click-Through Rate (CTR):**
  $$\text{CTR} = \frac{\text{Total Clicks}}{\text{Total Impressions}} \times 100$$
- **Engagement Rate (ER):**
  $$\text{Engagement Rate} = \frac{\text{Clicks} + \text{Shares} + \text{Comments}}{\text{Total Impressions}} \times 100$$
- **Conversion Rate (CR - Bottom of Funnel):**
  $$\text{Conversion Rate} = \frac{\text{Total Purchases}}{\text{Total Clicks}} \times 100$$
- **Purchase Rate (PR - Full Funnel Efficiency):**
  $$\text{Purchase Rate} = \frac{\text{Total Purchases}}{\text{Total Impressions}} \times 100$$

### 2. Dynamic Metric Switching (DAX Example)
```dax
Selected_Metric = 
SWITCH(
    SELECTEDVALUE('Select Dynamic Measure'[MeasureName], "Impressions"),
    "Impressions", [Total Impressions],
    "Clicks", [Total Clicks],
    "Purchases", [Total Purchases],
    "Engagements", [Total Engagements],
    [Total Impressions]
)
```

---

## 💡 Key Business Insights

| Metric / Dimension | Facebook | Instagram | Key Takeaway |
| :--- | :--- | :--- | :--- |
| **Impressions** | 216.0K | 123.8K | Facebook captures ~63.5% of total ad exposure. |
| **Clicks** | 25.4K | 14.7K | High link click volume across both channels. |
| **Purchases** | 1,323 | 708 | Facebook drove ~65% of total verified sales. |
| **CTR** | 11.76% | 11.86% | Instagram leads slightly in link click intent. |
| **Conversion Rate** | 5.21% | 4.82% | Facebook landing page traffic converts 8% higher into buyers. |

- **Top Ad Formats:** **Stories** deliver the highest exposure and CTR across both platforms, while **Video & Carousel** generate strong middle-funnel engagements.
- **Demographics:** The **18–34 age bracket** drives over 60% of total conversions; performance drops sharply past age 45.
- **Time Optimization:** Engagement peaks during afternoon and late evening hours; early morning hours (2 AM – 6 AM) show heavy drop-offs, indicating clear opportunity for dayparting schedule optimization.

---

## 🚀 How to Run Locally

1. **Clone this repository:**
   ```bash
   git clone [https://github.com/](https://github.com/)<your-username>/Meta-Ad-Performance-Analysis.git
   ```
2. Open **Power BI Desktop**.
3. Open `Meta Ad Performance Analysis.pbix`.
4. If a data source prompt appears:
   - Go to **Transform Data** > **Data source settings**.
   - Click **Change Source...** and browse to the CSV files inside the `Raw Data/` folder.
   - Click **Close & Apply**.

---

## 👤 Author & Acknowledgments

- **Author:** Vasu Bhardwaj
- **Domain:** Data Analytics & Performance Marketing Intelligence
- **Portfolio / Contact:** [LinkedIn Profile URL] | [Email Address]
