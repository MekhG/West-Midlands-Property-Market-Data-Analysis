# West-Midlands-Property-Market-Data-Analysis
A housing market analysis of West Midlands Local Authorities in England &amp; Wales, covering 2015 to 2021. Using official HM Land Registry Price Paid Data, the project tracks median house prices, sales volumes, year-on-year price changes, and includes a forecast to 2024 — broken down by geography, property type, build status, and month.

## 📊 Dashboard Preview

## 🗂️ Dataset
**Source:** HM Land Registry — House Price Statistics for Small Areas in England and Wales  
**Published:** 14 September 2022 | **Updated:** Quarterly  
**Coverage:** West Midlands Local Authorities | **Period:** 2015–2021

| Column | Description |
|---|---|
| `Month` | Calendar month of transaction |
| `Month Code` | Short month code (e.g. dec) |
| `Geography` | Local Authority (Birmingham, Coventry, Dudley etc.) |
| `PropertyType` | All, Detached, Flat/maisonette, Semi-detached, Terraced |
| `BuildStatus` | All, Existing, Newly built |
| `HouseSalesAndPrices` | Metric type (Count of sales, Mean price, Median price etc.) |
| `Year` | Year of data (2015–2021) |
| `Value` | Numeric value for the metric |

**Local Authorities Covered:** Birmingham, Coventry, Dudley, Herefordshire, Sandwell, Shropshire, Solihull, Stoke-on-Trent, Telford and Wrekin, Walsall, Wolverhampton

---

## 🔍 Key Findings

| Metric | Value |
|---|---|
| Avg Median Price (2021) | £214K |
| Avg Price Growth (2015–2021) | £43.7K |
| Total Transactions (2021) | 154K |
| Fastest Growing LA | Solihull (+44.8%) |

### Price Trend Insights
- House prices grew consistently from 2015 to 2021 across all LAs
- **2020 dip** visible in sales count — COVID-19 impact on transaction volumes
- **2021 rebound** was strong with YoY change reaching **118.3%** in sales activity
- **Solihull** led all local authorities with 44.8% price growth over the period

### Sales Volume Insights
- Birmingham dominates in absolute transaction count as the largest LA
- Sales count dropped sharply in **2020** across all LAs due to the pandemic
- **Newly built** properties command a premium over existing stock across all areas

### Forecast (2022–2024)
- Linear forecast models suggest continued upward pressure on mean prices
- Lower quartile prices projected to rise — affordability concerns for first-time buyers
- Sales count forecast shows moderate recovery trajectory post-2021

---

## 🛠️ Tools Used
- **Excel** — Data cleaning, pivot analysis, price trend exploration
- **Power BI** — Interactive multi-visual dashboard with:
  - KPI cards (Avg Median Price, Price Growth, Transactions, Fastest LA)
  - Sales vs Mean Price dual-axis line chart
  - YoY % Change bar chart
  - Price Trend and Sales Comparison grouped bar chart
  - Price and Sales Forecast with linear trend lines
  - Slicers: Geography, Property Type, Build Status, Year, Month

---

## 📁 Repository Structure
```
housing-market-analysis/
│
├── data/
│   └── housing_data.csv
│
├── excel/
│   └── housing_analysis.xlsx
│
├── dashboard/
│   └── housing_dashboard.pbix
│
└── README.md
```

---

## 📈 Analysis Steps
1. Loaded HM Land Registry data and explored structure in Excel
2. Filtered to West Midlands Local Authorities
3. Built pivot tables for price trends, sales counts, and YoY comparisons
4. Identified Solihull as fastest growing LA (44.8% gain)
5. Created dual-axis line chart for Sales vs Mean Price over time
6. Calculated YoY % change for each year and visualised as bar chart
7. Built price and sales forecast to 2024 using linear trend lines
8. Designed interactive Power BI dashboard with full slicer interactivity

---

## 📜 Data Source
> House Price Statistics for Small Areas in England and Wales — HM Land Registry Price Paid Data. Summary statistics for housing transactions by local authority, updated quarterly. Selecting a Year and Month returns data for the 12-month period ending that month and year.

---

## 🚀 How to Run
1. Clone the repo
2. Open `excel/housing_analysis.xlsx` for EDA
3. Open `dashboard/housing_dashboard.pbix` in Power BI Desktop
4. Use Geography, Property Type, Build Status, Year, and Month slicers to explore
