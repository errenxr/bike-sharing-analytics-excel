# Methodology

## 1. Dataset Overview

This project uses the Bike Sharing Dataset obtained from the UCI Machine Learning Repository.

**Dataset Information:**

- Dataset Name: Bike Sharing Dataset
- Source: UCI Machine Learning Repository
- Period: 2011–2012
- Data Granularity: Daily and hourly records
- Main Analysis Tool: Microsoft Excel

The dataset consists of two primary files:

| File | Description |
|---|---|
| `day.csv` | Daily bike rental records |
| `hour.csv` | Hourly bike rental records |

The dataset contains information about rental dates, seasons, weather conditions, working days, rental hours, and rental counts.

The rental count is divided into two user segments:

- `casual`: Rentals made by casual users.
- `registered`: Rentals made by registered users.
- `cnt`: Total number of bike rentals.

## 2. Data Preparation

The data preparation process was performed using Microsoft Excel.

### 2.1 Data Inspection

Initial inspection was conducted to understand the dataset structure, including:

- Number of rows and columns.
- Data types and column formats.
- Missing values.
- Relevant attributes for business analysis.
- Consistency between daily and hourly rental records.

### 2.2 Data Transformation

The hourly dataset was used as the primary source for building the master analysis dataset.

The following transformations were performed:

- Generated a complete date-hour combination covering 731 dates and 24 hours per day.
- Organized date and hourly information into a consistent structure.
- Added year information for easier comparison.
- Converted numerical month values into readable month names.
- Mapped season codes into descriptive season names.
- Grouped hours into four time periods: Morning, Afternoon, Evening, and Night.
- Converted the working day indicator into descriptive categories: Working Day and Non-Working Day.
- Retrieved hourly casual, registered, and total rental counts using Excel SUMIFS formulas.

### 2.3 Handling Missing Date-Hour Combinations

The hourly dataset contains fewer records than the complete combination of 731 dates and 24 hours.

Missing date-hour combinations were reconstructed with zero rental counts for the corresponding hourly rental measures.

This assumption was supported by comparing the aggregated hourly rental counts with the daily rental totals in `day.csv`, which showed matching daily totals.

This reconstruction was applied only to the rental count measures and does not imply that other missing hourly attributes were reconstructed.

### 2.4 Master Analysis Dataset

A consolidated dataset named `Data Master` was created to support the analysis.

It contains the following attributes:

| Attribute | Description |
|---|---|
| `dteday` | Rental date |
| `yr_inf` | Year (2011 or 2012) |
| `month` | Numerical month (1–12) |
| `mnth_information` | Descriptive month name |
| `hr` | Rental hour (0–23) |
| `season_info` | Season category |
| `timeinformation` | Time period category |
| `workingday` | Original working day indicator |
| `workday_desc` | Working Day or Non-Working Day |
| `casual` | Casual rental count |
| `registered` | Registered rental count |
| `cnt` | Total rental count |

The total rental count is calculated as:

`cnt = casual + registered`

## 3. Exploratory Data Analysis (EDA)

Exploratory Data Analysis was conducted to identify patterns and relationships in bike rental demand.

The analysis focused on four main areas:

### 3.1 Hourly Rental Demand

Analyzed average rental counts by hour to identify peak rental hours and compare hourly demand patterns between working days and non-working days.

### 3.2 Customer Segment Analysis

Compared casual and registered rental counts across different seasons to understand segment contributions and seasonal behavior.

### 3.3 Monthly Rental Trends

Examined total rental counts by month and year to identify changes in demand over time.

### 3.4 Time Period Distribution

Analyzed total rental counts across Morning, Afternoon, Evening, and Night to understand demand distribution throughout the day.

## 4. Data Analysis Techniques

The following Excel features and techniques were used:

- **PivotTables:** Aggregating rental data across different dimensions.
- **Excel Formulas:** SUMIFS, AVERAGE, XLOOKUP, SUM, IF, IFS, and other supporting formulas.
- **Data Aggregation:** Calculating total and average rental counts.
- **Comparative Analysis:** Comparing rental demand across hours, seasons, years, and user segments.
- **Data Visualization:** Presenting analytical results through charts and KPI cards.
- **Interactive Slicers:** Enabling dynamic filtering by year, season, month, working day, and time period.

## 5. Dashboard Development

An interactive Excel dashboard was developed to summarize the analytical findings.

The dashboard includes:

- Key Performance Indicators (KPIs).
- Hourly rental demand charts.
- Working day vs. non-working day comparisons.
- Seasonal customer segment analysis.
- Monthly rental trend visualizations.
- Time period rental distribution.
- Interactive Slicers for data exploration.

## 6. Tools and Technologies

- Microsoft Excel
- PivotTables
- Excel Formulas
- Interactive Slicers
- Data Cleaning and Transformation
- Exploratory Data Analysis (EDA)
- Data Visualization

## 7. Analysis Limitations

Several limitations should be considered when interpreting the results:

- The dataset covers only the 2011–2012 period.
- Casual and registered values represent rental counts, not unique customer counts.
- Revenue, pricing, and operational costs are not included.
- Individual customer identifiers are unavailable.
- The analysis does not directly measure customer retention or profitability.
- The reconstructed missing date-hour combinations rely on the assumption that their rental counts are zero, supported by daily total reconciliation.