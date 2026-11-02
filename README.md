# Bike Sharing Analytics Dashboard | Excel Data Analysis

An exploratory data analysis project using Microsoft Excel to analyze bike rental demand, customer segment behavior, and seasonal trends. This project transforms historical bike-sharing data into actionable business insights through data preparation, PivotTables, interactive Slicers, and dashboard visualizations.

## Dashboard Preview

![Bike Sharing Dashboard](images/Dashboard_(horizontal).png)

*An interactive Excel dashboard featuring key performance indicators, rental demand analysis, customer segment comparisons, and dynamic filtering.*

## Project Overview

Bike-sharing services generate valuable operational data that can help businesses understand customer behavior and rental demand patterns.

This project explores the Bike Sharing Dataset from the UCI Machine Learning Repository, covering rental records from 2011 to 2012.

The analysis focuses on identifying peak rental hours, comparing demand between working and non-working days, examining customer segment contributions, and understanding seasonal and monthly rental trends.

The results are presented in an interactive Microsoft Excel dashboard to support data-driven business decisions.

## Business Objectives

- Identify peak rental hours and understand hourly demand patterns.
- Compare bike rental activity between working days and non-working days.
- Analyze rental behavior across casual and registered user segments.
- Examine seasonal and monthly rental trends.
- Understand rental distribution across different periods of the day.
- Develop actionable recommendations for operational planning and customer engagement.

## Business Questions

The project addresses the following business questions:

1. **Hourly Rental Demand:** How does bike rental demand vary by hour and working day, and during which hours should the company increase bike availability?

2. **Customer Segment Analysis:** How do rental patterns differ between casual and registered users across seasons, and which segment should be prioritized in marketing strategies?

3. **Monthly Rental Trends:** How does bike rental demand change across months and years?

4. **Time Period Analysis:** How is rental demand distributed across Morning, Afternoon, Evening, and Night?

## Dataset

**Source:** [UCI Machine Learning Repository – Bike Sharing Dataset](https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset)

**Citation:**

Fanaee-T, H. (2013). *Bike Sharing Dataset*. UCI Machine Learning Repository. https://doi.org/10.24432/C5W894

### Dataset Information

| Attribute | Description |
|---|---|
| Period | 2011–2012 |
| Daily Records | 731 |
| Hourly Records | 17,379 |
| Daily Dataset | `day.csv` |
| Hourly Dataset | `hour.csv` |

The dataset contains information about rental dates, seasons, weather conditions, working days, rental hours, and rental counts.

### Key Variables

| Variable | Description |
|---|---|
| `dteday` | Rental date |
| `season` | Season category |
| `yr` | Year indicator |
| `mnth` | Month |
| `hr` | Rental hour |
| `workingday` | Working day indicator |
| `casual` | Casual rental count |
| `registered` | Registered rental count |
| `cnt` | Total rental count |

**Note:** Casual and registered values represent rental counts, not unique customer counts.

## Tools & Technologies

- Microsoft Excel
- PivotTables
- Excel Formulas (SUMIFS, AVERAGEIFS, XLOOKUP)
- Interactive Slicers
- Data Cleaning and Transformation
- Exploratory Data Analysis (EDA)
- Data Visualization

## Methodology

The project was conducted through the following stages:

### 1. Data Understanding and Inspection
- Examined the structure, attributes, and data types of the daily and hourly datasets.
- Identified relevant variables for business analysis.
- Checked missing values and data consistency.

### 2. Data Preparation and Transformation
- Generated a complete date-hour structure covering 731 dates and 24 hours per day.
- Transformed numerical month and season codes into descriptive categories.
- Grouped rental hours into Morning, Afternoon, Evening, and Night.
- Converted the working day indicator into Working Day and Non-Working Day categories.
- Aggregated hourly rental counts using Excel formulas.
- Created a consolidated `Data Master` worksheet.

### 3. Exploratory Data Analysis
- Analyzed average rental counts by hour.
- Compared hourly demand between working days and non-working days.
- Examined casual and registered rental counts across seasons.
- Explored monthly rental trends across years.
- Analyzed rental distribution across different time periods.

### 4. Dashboard Development
- Created PivotTables for different business questions.
- Implemented interactive Slicers for dynamic data filtering.
- Designed KPI cards and data visualizations.
- Consolidated key business insights into an interactive Excel dashboard.

## Key Business Insights

The analysis identified several important findings:

| Business Insight | Result |
|---|---|
| Peak Rental Hour | 17:00 (5:00 PM) |
| Average Rentals at Working Day | 191,034 |
| Average Rentals at Non-Working Day | 180,424 |
| Highest Rental Season | Fall |
| Highest Seasonal Rental Volume | 1,061,129 rentals |
| Registered User Contribution | 81.17% |
| Casual User Contribution | 18.83% |

### 1. Hourly Rental Demand

The highest average rental activity occurs at 17:00, indicating a peak in late-afternoon demand.

### 2. Working Day vs. Non-Working Day

Rental patterns vary between working days and non-working days. Understanding these differences can help the company plan operational resources according to demand.

### 3. Customer Segment Contribution

Registered users account for 81.17% of total rentals, while casual users contribute 18.83%.

This highlights the importance of maintaining registered user engagement while exploring opportunities to attract casual users.

### 4. Seasonal Rental Trends

Fall records the highest seasonal rental volume, with 1,061,129 rentals during the analyzed period.

## Business Recommendations

Based on the analytical findings, several recommendations can be considered:

**1. Optimize Bike Availability**
- Prepare sufficient bike availability before peak rental hours.
- Monitor hourly demand to improve operational planning.
- Consider different demand patterns between working days and non-working days.

**2. Strengthen Customer Retention**
- Maintain engagement with registered users.
- Explore loyalty programs and membership benefits.
- Monitor registered rental activity over time.

**3. Improve Casual User Acquisition**
- Develop targeted promotions for casual users.
- Introduce attractive short-term rental offers.
- Explore opportunities to convert casual users into registered members.

**4. Support Seasonal Planning**
- Use historical seasonal patterns to support resource allocation.
- Prepare promotional campaigns ahead of periods with higher rental activity.
- Monitor monthly and seasonal demand changes.

## Dashboard Features

The Excel dashboard includes:

- **KPI Cards:** Peak Rental Hour, Average Rentals at Working Day, Average Rentals at Non-Working Day, and Highest Rental Season.
- **Hourly Rental Analysis:** Visualizes average rental demand by hour.
- **Working Day Comparison:** Compares rental patterns between working days and non-working days.
- **Customer Segment Analysis:** Compares casual and registered rental activity across seasons.
- **Monthly Rental Trends:** Displays rental volume across months and years.
- **Time Period Distribution:** Shows rental distribution across different periods of the day.
- **Interactive Slicers:** Filters analysis by year, season, month, working day, and time period.

## Repository Structure

```text
bike-sharing-analytics-excel/
│
├── README.md
│
├── data/
│   └── raw/
│       ├── day.csv
│       ├── hour.csv
│       └── Readme.txt
│
├── processed data & dashboard/
│   ├── bike_sharing_analysis.xlsx
│   ├── dashboard (vertical).pdf
│   └── dashboard (horizontal).png
│
├── analysis/
│   ├── business_understanding.md
│   ├── methodology.md
│   └── key_findings.md
│
├── images/
│   ├── Average by Hour of The Day.png
│   ├── Dashboard_(horizontal).png
│   ├── Monthly Rental Tren.png
│   ├── Rental Distribution by Time Periode.png
│   ├── Seasonal Customer Segment.png
│   └── Working Day VS Non-working Day.png
│
├── .gitignore
└── LICENSE
```

## Project Files

- **Excel Dashboard:** `processed data & dashboard/bike_sharing_analytics.xlsx` – Contains the complete dataset preparation, PivotTables, and interactive dashboard.
- **Dashboard PDF:** `processed data & dashboard/dashboard (vertical).pdf` – A static version of the dashboard for quick viewing.
- **Analysis Documentation:** `analysis/` – Contains business questions, methodology, and key findings.

## Limitations

- The dataset covers only the 2011–2012 period.
- Rental counts do not represent unique customers.
- Revenue, pricing, and operational costs are not available.
- Individual customer identifiers are not included.
- The analysis does not directly measure customer retention or profitability.
- Missing date-hour combinations were reconstructed with zero rental counts, supported by reconciliation against daily rental totals.

## Conclusion

This project demonstrates how Microsoft Excel can be used to perform exploratory data analysis, identify business patterns, and communicate findings through an interactive dashboard.

The analysis provides insights into hourly rental demand, working-day patterns, customer segment contributions, and seasonal trends. These findings can support operational planning and customer engagement strategies in bike-sharing services.

## Author

**Annisa Nabila Putri**

Computer Engineering Graduate | Aspiring Data Analyst & Data Scientist

[LinkedIn](https://www.linkedin.com/in/annisanabilaaputri/) | [GitHub](https://github.com/errenxr)

## References

Fanaee-T, H. (2013). *Bike Sharing Dataset*. UCI Machine Learning Repository.