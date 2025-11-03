# Labor-Market-Analysis-Forecasting

## Overview
This project analyzes U.S. labor market trends using data from the Federal Reserve Economic Data (FRED) API. It includes historical analysis, feature engineering, correlation studies, and time series forecasting for key labor market metrics such as Unemployment Rate, Avg Hourly Earnings, and Job Openings.

The analysis showcases skills in Python, Pandas, Prophet forecasting, and data visualization, providing insights into labor market dynamics, wage trends, and macroeconomic cycles.

---

## Data Sources
Data was pulled from FRED using the `fredapi` library. The following series were used:

| Metric                          | FRED Series Code |
|---------------------------------|----------------|
| Unemployment Rate               | UNRATE          |
| Labor Force Participation       | CIVPART         |
| Job Openings                    | JTSJOL          |
| Avg Hourly Earnings             | CES0500000003   |
| CPI Inflation                   | CPIAUCSL        |
| Recession Indicator             | USREC           |

**Engineered Features:**
- Job Openings per Unemployed  
- YoY percentage changes (Unemployment Rate, Avg Hourly Earnings, CPI)  
- Real Wage Growth (adjusted for CPI)  
- 3-month rolling averages for trend visualization  

---

## Analysis
**Core Labor Market Relationships:**
- Unemployment Rate and Job Openings: strong negative correlation (-0.682), highlighting labor market slack.  
- Job Openings per Unemployed: even stronger negative correlation (-0.796), showing market tightness.  
- Labor Force Participation shows nuanced relationships with unemployment and openings, suggesting workforce supply dynamics.

**Wage & Inflation Relationships:**
- Avg Hourly Earnings and CPI Inflation: extremely high positive correlation (0.993), indicating wages track inflation closely.  
- Real Wage Growth correlates positively with Job Openings (0.778) and negatively with Unemployment Rate (-0.33), reflecting tight labor market pressure on wages.

**Recession Context:**
- Recessions moderately affect unemployment, job openings, and real wages, emphasizing how macroeconomic cycles influence labor market outcomes.

---

## Forecasting
Time series forecasting was conducted using **Prophet**:

- **Unemployment Rate:** Declined from 2009–2019, impacted by COVID-19, with gradual stabilization post-2023. Forecast shows a steady long-term trend.  
- **Avg Hourly Earnings:** Forecast shows gradual growth, tracking inflation trends.  
- **Job Openings:** Forecast highlights early decline, recovery through 2024, and a spike during periods of tight labor markets.

All forecasts include rolling averages and recession shading to contextualize trends.

---

## Visualizations
Key visualizations generated and included in `visuals/`:

- **Correlation Heatmap** – relationships between core labor market variables  
- **Forecast Plots** – Unemployment Rate, Avg Hourly Earnings, Job Openings, including rolling averages and forecast confidence intervals  
- **Recession Shading** – highlights periods of economic downturn  

---

## Tableau Dashboard:
- Link: https://public.tableau.com/views/U_S_LaborMarketTrendsDashboard/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
- Notes: Only had access to Tableau Public on the Web browswer
