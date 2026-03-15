# West Midlands Property Market Data Analysis

## Introduction / Description
This project provides a comprehensive analysis of the housing market across West Midlands Local Authorities in England and Wales from 2015 to 2021. Using official HM Land Registry Price Paid Data, it examines median house prices, sales volumes, and year-on-year price changes, with a forecast extending to 2024. The analysis is broken down by geography, property type, build status, and month, offering insights into trends and market dynamics in the region. 

A detailed presentation with insights and recommendations is presented through West Midlands Property Market pdf

## Dashboard Preview
<img width="632" height="334" alt="image" src="https://github.com/user-attachments/assets/263ca286-571d-40c3-a9d7-f92ee29893b9" />

<img width="678" height="373" alt="image" src="https://github.com/user-attachments/assets/0a8558cd-1fc9-48dc-977c-83497efbc799" />


*Interactive Power BI dashboard allows filtering by Geography, Property Type, Build Status, Year, and Month to explore detailed trends and forecasts.*

## Objective
- Analyze historical housing market trends in the West Midlands.  
- Identify local authorities with fastest price growth and highest transaction volumes.  
- Forecast property prices and sales trends up to 2024.  
- Provide actionable insights for buyers, investors, and policymakers.  

## Dataset Preview
**Source:** HM Land Registry — House Price Statistics for Small Areas in England and Wales  
**Coverage:** West Midlands Local Authorities | **Period:** 2015–2021  

| Column | Description |
|--------|-------------|
| Month | Calendar month of transaction |
| Month Code | Short month code (e.g., dec) |
| Geography | Local Authority (Birmingham, Coventry, Dudley, etc.) |
| PropertyType | All, Detached, Flat/maisonette, Semi-detached, Terraced |
| BuildStatus | All, Existing, Newly built |
| HouseSalesAndPrices | Metric type (Count of sales, Mean price, Median price, etc.) |
| Year | Year of data (2015–2021) |
| Value | Numeric value for the metric |

**Local Authorities Covered:** Birmingham, Coventry, Dudley, Herefordshire, Sandwell, Shropshire, Solihull, Stoke-on-Trent, Telford and Wrekin, Walsall, Wolverhampton  

## Tools and Methods Used
- **Excel:** Data cleaning, pivot analysis, exploratory analysis, trend visualization.  
- **Power BI:** Interactive dashboard with KPI cards, dual-axis line charts, bar charts, forecasts, and slicers for dynamic exploration.  
- **SQL (SQLite via Python/Kaggle):** Trend analysis, YoY percentage calculation, median prices, and sales aggregation.  

## Analysis Steps
1. Loaded HM Land Registry Price Paid Data and explored structure in Excel.  
2. Filtered dataset for West Midlands Local Authorities.  
3. Built pivot tables to analyze price trends, sales counts, and YoY changes.  
4. Identified fastest growing Local Authority: **Solihull** (+44.8% median price growth).  
5. Created dual-axis line chart for **Sales vs Mean Price** over time.  
6. Calculated YoY percentage changes and visualized using bar charts.  
7. Forecasted prices and sales to 2024 using linear trend lines.  
8. Developed an interactive Power BI dashboard with slicers for Geography, Property Type, Build Status, Year, and Month.  

## Key Findings
- **Average Median Price (2021):** £214K  
- **Average Price Growth (2015–2021):** £43.7K  
- **Total Transactions (2021):** 154K  
- **Fastest Growing LA:** Solihull (+44.8%)  

**Price Trends:**  
- Consistent price growth across all local authorities from 2015–2021.  
- Sales volumes dipped in 2020 due to COVID-19 but rebounded strongly in 2021.  
- Newly built properties command higher prices across all areas.  

**Sales Volume Insights:**  
- Birmingham has the highest transaction count due to its size.  
- Moderate sales recovery is expected post-2021.  

**Forecast (2022–2024):**  
- Linear forecast models indicate continued upward pressure on mean prices.  
- Lower quartile prices are projected to rise, raising affordability concerns for first-time buyers.  
- Sales counts expected to recover moderately.  

## Business Insights and Recommendations

**For Home Buyers / First-Time Buyers:**  
- **Target affordability:** Focus on areas with lower median prices or slower growth (e.g., Dudley, Walsall) to enter the market without overpaying.  
- **Consider newly built properties:** These generally command a premium but offer modern amenities and long-term value.  
- **Monitor forecast trends:** Lower quartile prices are projected to rise; first-time buyers may need to act sooner to secure more affordable options.  

**For Property Investors:**  
- **High-growth opportunities:** Invest in **Solihull**, which saw +44.8% growth, or other areas showing consistent upward trends.  
- **Volume-driven strategy:** Birmingham has the highest transaction count; high liquidity reduces risk for resale or rental purposes.  
- **Diversify across property types:** Detached and semi-detached homes show strong growth trends; consider balancing portfolio across types.  

**For Developers / Builders:**  
- **Focus on premium builds:** Newly built homes consistently command higher prices — targeting high-demand areas maximizes ROI.  
- **Plan inventory based on market trends:** High-demand LAs with rapid price growth require careful planning to match supply with buyer affordability.  
- **Future-proof properties:** Integrate energy efficiency and modern amenities to justify higher pricing as market demand evolves.  

**For Policymakers / Urban Planners:**  
- **Address affordability:** Monitor forecasted price increases to support first-time buyers with incentives or housing schemes.  
- **Urban development planning:** Prioritize infrastructure and housing support in high-growth areas like Solihull to sustain market balance.  
- **Track transaction trends:** COVID-19 caused temporary dips; understanding volume changes helps plan for future market shocks.  

**Actionable Dashboard Insights:**  
- Use slicers to explore price trends by **Local Authority, Property Type, Build Status, and Month**.  
- Compare YoY % change across areas to identify emerging growth pockets.  
- Forecast trends help anticipate affordability challenges and plan investment or development strategies. 


## How to Run
1. Clone the repository:  
   ```bash
   git clone <repo-url>

2. Explore data in Excel: housing_analysis.xlsx
3. Run SQL queries in Python: housing_data_queries.ipynb
4. Open interactive dashboard: housing_dashboard.pbix
5. Use slicers for dynamic exploration of trends and forecasts.
