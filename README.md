\# 🏥 Clinical Data Analysis Dashboard  
### Hospital Performance & Healthcare Metrics Intelligence

---

## 📌 Project Overview

This Power BI project provides a comprehensive analytical view of hospital clinical performance using key healthcare indicators across multiple hospitals and years.

The dashboard delivers actionable insights into:

- Infection trends  
- Readmission rates  
- Hospital admissions  
- Mortality rates  
- Hospital-level performance comparison  
- Year-over-Year (YoY) analysis  

The objective is to enable healthcare decision-makers to monitor operational efficiency, patient safety, and overall hospital performance using interactive visual analytics.

---

## 🎯 Business Problem

Healthcare institutions must continuously monitor clinical performance to:

- Reduce infection rates  
- Minimize patient readmissions  
- Improve survival outcomes  
- Optimize hospital capacity  
- Detect performance inconsistencies across facilities  

Without centralized analytics, identifying trends and anomalies becomes inefficient.

This dashboard solves that by transforming raw hospital data into structured KPIs and trend analysis.

---

## 📊 Dashboard Structure

The report consists of two main analytical pages:

---

# 📄 Page 1: Analysis by Year

## Key Yearly Metrics

### 1️⃣ Number of Infections by Year
Tracks infection trends over time.

Observations:
- Initial peak around 4,990K
- Decline in mid-years
- Noticeable spike again before stabilizing

Insight:
Infection rates show fluctuation patterns, indicating possible seasonal or policy-driven impacts.

---

### 2️⃣ Number of Readmissions by Year

Tracks patient return rates after discharge.

Observations:
- Highest at 14,302K
- Drop in mid-years
- Recovery trend in later years

Insight:
Readmission spikes may reflect discharge quality or chronic disease management gaps.

---

### 3️⃣ Number of Admissions by Year

Hospital intake capacity and patient volume tracking.

Observations:
- Stable around 310M admissions
- Slight fluctuations year-over-year

Insight:
Admissions remain consistently high, indicating sustained operational load.

---

### 4️⃣ Number of Deaths by Year

Mortality tracking across years.

Observations:
- Highest around 2,494K
- Dip in mid-cycle
- Mild upward adjustment later

Insight:
Mortality trends appear correlated with infection and readmission fluctuations.

---

## KPI Cards (Top Summary Metrics)

- Total yearly infection volume
- Total readmissions
- Total admissions
- Total deaths

---

# 📄 Page 2: Hospital-Level Analysis

This page focuses on performance comparison across Hospital IDs.

---

## 🏥 Metrics by Hospital ID

### 1️⃣ Infections by Hospital
- Most hospitals stable around 4.00M
- One hospital significantly lower (~2.83M)

Insight:
Performance disparity suggests operational or demographic differences.

---

### 2️⃣ Readmissions by Hospital
- Majority around 11.5M
- One hospital significantly lower (~8.1M)

Insight:
Potential outlier requiring deeper quality analysis.

---

### 3️⃣ Admissions by Hospital
- Most at ~249M
- One hospital lower (~176M)

Insight:
Lower admissions may indicate smaller facility capacity.

---

### 4️⃣ Deaths by Hospital
- Most hospitals around 2.00M
- One hospital at 1.41M

Insight:
Mortality performance varies significantly across facilities.

---

## 🛠️ Tools & Technologies Used

- Power BI Desktop
- Power Query (Data Cleaning & Transformation)
- DAX (Measures & Aggregations)
- Data Modeling
- Interactive Filters & Slicers
- Custom UI Layout Design

---

## 📈 Core DAX Measures (Example Logic)

### Total Infections
```DAX
Total Infections = SUM(HospitalData[Infections])
```

### Total Readmissions
```DAX
Total Readmissions = SUM(HospitalData[Readmissions])
```

### Total Admissions
```DAX
Total Admissions = SUM(HospitalData[Admissions])
```

### Total Deaths
```DAX
Total Deaths = SUM(HospitalData[Deaths])
```

### Year-over-Year Change Example
```DAX
YoY Infections % =
DIVIDE(
    [Total Infections] - CALCULATE([Total Infections], SAMEPERIODLASTYEAR(Date[Date])),
    CALCULATE([Total Infections], SAMEPERIODLASTYEAR(Date[Date]))
)
```

---

## 🎨 Design & UX Strategy

- Clean clinical-themed color palette (teal/medical tone)
- Large KPI-driven headers
- Area charts for trend visibility
- Line charts for comparison
- Balanced layout with visual symmetry
- Hospital performance segmentation
- Easy filtering between years and facilities

---

## 📊 Key Insights

✔ Infection and readmission rates show cyclical fluctuations  
✔ Mortality trends appear partially correlated with infection spikes  
✔ One hospital consistently reports lower volume metrics  
✔ Admissions remain high and stable across years  
✔ Performance benchmarking enables targeted hospital audits  

---

## 🚀 What This Project Demonstrates

- Healthcare KPI modeling
- Multi-page dashboard architecture
- Year-based time intelligence
- Hospital benchmarking analysis
- Advanced DAX aggregation
- Clean executive-level visualization design
- Real-world healthcare analytics application

---

## 🧠 Potential Enhancements

- Infection-to-Death correlation analysis
- Readmission Rate per Admission Ratio
- Risk-adjusted mortality index
- Predictive forecasting (Time Series Model)
- Hospital performance scoring index
- Drill-through to patient-level segmentation

---

## 👩‍💻 Author

Sara Alfayez

---
