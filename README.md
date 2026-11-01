# West Midlands Property Market Analysis (2015–2021)

![Excel](https://img.shields.io/badge/Excel-pivots_&_forecasts-217346?logo=microsoftexcel&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-DuckDB-FFF000?logo=duckdb&logoColor=black)
![Power BI](https://img.shields.io/badge/Power_BI-dashboard-F2C811?logo=powerbi&logoColor=black)

An analysis of house prices and sales across the 11 local authorities of the West Midlands from 2015 to 2021, built in **Excel**, **SQL (DuckDB in Python)** and **Power BI**, with a trend forecast to 2024. It answers three questions: *where have prices grown fastest, where is the market most active, and what does that mean for buyers, investors and planners?*

<img width="632" alt="Power BI dashboard: price trends by local authority" src="https://github.com/user-attachments/assets/263ca286-571d-40c3-a9d7-f92ee29893b9" />

---

## Key findings

Figures are year-ending December, all property types and build statuses, unless stated.

| | |
|---|---|
| **Fastest median price growth, 2015–2021** | **Birmingham, +44.8%** (£145K → £210K) |
| **Most expensive area** | Solihull, £320K median in 2021 (but 9th of 11 for growth, +33.3%) |
| **Most affordable area** | Stoke-on-Trent, £134K median in 2021 |
| **Most active market** | Birmingham, the largest number of sales in every year |
| **COVID effect** | Sales fell 19% in 2020 (47.3K → 38.2K) and recovered to 48.7K in 2021 |

- **Growth was strongest in the more affordable urban areas.** After Birmingham came Coventry (+41.4%), Sandwell (+40.1%) and Wolverhampton (+39.8%). The priciest areas, Solihull and Herefordshire, were among the slowest growers, so prices across the region converged slightly.
- **New builds carry a premium in all 11 areas.** It ranges from almost nothing in Coventry and Solihull to about £100K in Stoke-on-Trent (£233K new vs. £132K existing, 2021).
- **Property type matters.** Semi-detached homes grew most (+40%, region-wide median); flats and maisonettes grew least (+23%).
- **Entry-level prices are rising too.** Lower-quartile prices rose by an average of 37% between 2015 and 2021, which puts pressure on first-time buyers.

---

## What it means

**First-time buyers:** Stoke-on-Trent, Sandwell and Wolverhampton have the lowest medians, but the last two are also among the fastest risers, so affordability there is shrinking.

**Investors:** Birmingham combines the fastest price growth with the deepest market, so the most liquidity when it is time to sell. Solihull offers prestige and high prices but below-average growth.

**Developers:** The new-build premium and strong demand for semi-detached homes point to family housing as the best-supported product.

**Policymakers:** Fast growth at the affordable end of the market (lower quartile +37%) is where first-time-buyer support is most needed.

---

## Dataset

**Source:** House Price Statistics for Small Areas (HPSSA), derived from HM Land Registry Price Paid Data.
**Coverage:** 11 West Midlands local authorities in England, 2015–2021, quarterly snapshots (March, June, September, December), each covering the 12 months to that point.

| Column | Description |
|--------|-------------|
| `Month`, `Month code` | Quarter-end month of the rolling 12-month figure |
| `Geography` | Local authority |
| `PropertyType` | All, Detached, Flat/maisonette, Semi-detached, Terraced |
| `BuildStatus` | All, Existing, Newly built |
| `HouseSalesAndPrices` | Count of sales, Mean, Median, Lower quartile or Tenth percentile price |
| `Year` | 2015–2021 |
| `Value` | The figure for that metric |

**Local authorities:** Birmingham, Coventry, Dudley, Herefordshire, Sandwell, Shropshire, Solihull, Stoke-on-Trent, Telford and Wrekin, Walsall, Wolverhampton.

---

## How it was built

1. **Excel:** cleaned and explored the data with pivot tables, ranked local authorities by price growth, and charted year-on-year change.
2. **SQL:** loaded the data into **DuckDB** from pandas and wrote queries for yearly sales, mean and median price trends and year-on-year change ([`sql_queries`](sql_queries)).
3. **Forecast:** projected prices and sales to 2024 with linear trend lines.
4. **Power BI:** built an interactive dashboard with KPI cards, a dual-axis sales-vs-price chart and slicers for geography, property type, build status, year and month.
5. **Report:** wrote a 14-page slide-style report with recommendations.

<img width="678" alt="Power BI dashboard: sales volumes and forecast" src="https://github.com/user-attachments/assets/0a8558cd-1fc9-48dc-977c-83497efbc799" />

---

## Repository contents

| File | What it is |
|---|---|
| [`HouseBook.xlsx`](HouseBook.xlsx) | The dataset (23,000+ rows) |
| [`Housing_data_dashboard.pbix`](Housing_data_dashboard.pbix) | Power BI dashboard (open in Power BI Desktop) |
| [`sql_queries`](sql_queries) | DuckDB SQL queries, run from Python/pandas |
| [`West+Midlands+Property+Market…pdf`](West+Midlands+Property+Market_+Data+Analysis+and+Strategic+Insights.pdf) | Slide-style report with recommendations |

## How to run

```bash
git clone https://github.com/MekhG/West-Midlands-Property-Market-Data-Analysis.git
cd West-Midlands-Property-Market-Data-Analysis
```

- **Dashboard:** open `Housing_data_dashboard.pbix` in Power BI Desktop and use the slicers.
- **SQL:** in a notebook, `pip install duckdb pandas openpyxl`, then run the cells in `sql_queries` from the repository folder (they read `HouseBook.xlsx` directly).
- **Note:** each row is a rolling 12-month figure, so add up sales from one quarter-end month (e.g. December) only. Summing all four months counts each sale up to four times.
