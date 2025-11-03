# SQL Insights for Retail Sales

**Version:** SQL-Focused Analytics | **Tools:** PostgreSQL / MySQL, Optional Python & Tableau

---

## Overview
This project analyzes **50K+ e-commerce transactions** to uncover customer behavior, sales trends, and product performance using **advanced SQL techniques**.  
It demonstrates the ability to write **complex queries, use window functions, CTEs, and aggregations** to generate actionable business insights.

---

## Objectives
- Build and query a relational database simulating real-world retail operations.  
- Extract insights on **sales trends, customer behavior, and product performance**.  
- Showcase advanced SQL skills through **joins, aggregations, window functions, and CASE logic**.  
- Optionally integrate Python or Tableau for visualization and further analysis.

---

## Tech Stack
| Category | Tools / Libraries |
|-----------|-------------------|
| **Database** | PostgreSQL / MySQL |
| **SQL Concepts** | JOINs, Aggregations (SUM, COUNT, AVG), CTEs, Window Functions (RANK, DENSE_RANK, LAG, LEAD), CASE logic |
| **Optional Tools** | Python (for data loading), Tableau (for visualization) |
| **Workflow** | SQL-based ETL, Analysis, Reporting |

---

## Dataset Structure
The synthetic dataset is designed to mimic real-world retail data:  

| Table | Key Columns |
|-------|-------------|
| **Customers** | customer_id, name, region, signup_date |
| **Products** | product_id, product_name, category, unit_price |
| **Orders** | order_id, customer_id, order_date, total_amount, payment_method |
| **Order_Details** | order_detail_id, order_id, product_id, quantity, unit_price |
| **Returns** | return_id, order_id, product_id, return_reason, return_date |

---

## Analysis Pipeline
1. **Database Setup**  
   - Loaded CSV datasets into relational tables.  
   - Defined primary keys, foreign keys, and indices for query efficiency.  

2. **Exploratory SQL Queries**  
   - Calculated revenue, order frequency, and customer lifetime value.  
   - Aggregated product performance by category and region.  

3. **Advanced SQL Techniques**  
   - **CTEs** to organize complex queries.  
   - **Window Functions** for ranking products and tracking trends over time.  
   - **CASE logic** to categorize revenue, returns, and customer segments.

---

## Optional Visualization(In-Progress)
- Integrated results in **Tableau** to create interactive dashboards.  
- Key visualizations:  
  - Revenue by product category and region  
  - Top 10 products by total revenue  
  - Monthly revenue trends (YoY)  
  - Customer lifetime value distribution  

### 🔗 Tableau Dashboard (In-Progress)
*(Optional if integrated)*  
**[View Dashboard →](#)**  

---

## 🧾 File Structure
SQL-Insights-for-Retail-Sales/
│
├── data/
│ ├── raw/ # Original CSV files
│ └── loaded/ # Tables loaded into SQL database
│
├── notebooks/ # Optional Python analysis notebooks
│ └── analysis_visualization.ipynb
│
├── sql/
│ ├── schema.sql # Table creation and constraints
│ ├── data_load.sql # Load CSVs into tables
│ └── queries.sql # Advanced analysis queries
│
├── visuals/ # Optional exported charts
└── README.md

---

## Results & Insights

### Key Findings
- **Top 10 products** accounted for **35% of total revenue**, indicating concentration in high-performing SKUs.  
- **Returning customers** contributed **X% of total revenue**, highlighting their importance to the business.  
- **Regions with highest LTV** can be targeted for marketing campaigns.  
- **Monthly revenue trends** revealed seasonal peaks and slow periods for inventory planning.

### Key Takeaway
This project demonstrates **advanced SQL proficiency** for real-world analytics.  
It highlights the ability to **transform raw transaction data into actionable business insights** using relational databases, complex queries, and optional visualization tools.


## Author
**Galen Pike**  
Data Analyst | SQL • Python • Tableau  
[LinkedIn Profile](#) | [Portfolio](3)

---
