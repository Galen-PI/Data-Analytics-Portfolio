# E-Commerce Sales Analysis

**Version:** End-to-End Analysis | **Tools:** Python, Pandas, Tableau, scikit-learn

---

## Overview
This project analyzes **42K+ e-commerce transactions** to uncover sales trends, customer behavior, and pricing insights.  
It demonstrates a **complete analytics workflow** from data cleaning and metric derivation to predictive modeling and interactive visualization.

---

## Objectives
- Clean and standardize raw e-commerce data.  
- Derive metrics such as **purchase efficiency**, **discount effectiveness**, and **price brackets**.  
- Conduct exploratory data analysis to uncover trends, outliers, and anomalies.  
- Build predictive models (Linear Regression & Random Forest) to identify key sales drivers.  
- Generate actionable insights for **pricing, marketing, and discount strategy**.

---

## Tech Stack
| Category | Tools / Libraries |
|-----------|-------------------|
| **Language** | Python |
| **Libraries** | Pandas, NumPy, Matplotlib, Seaborn, scikit-learn |
| **Tools** | Jupyter Notebook, VS Code |
| **Visualization** | Seaborn, Matplotlib, Tableau |
| **Workflow** | Automated ETL Pipeline (Extract → Transform → Clean → Aggregate → Analyze) |

---

## Dataset
- **Source:** [Amazon Products Sales Dataset (42K+ transactions)](https://www.kaggle.com/datasets/ikramshah512/amazon-products-sales-dataset-42k-items-2025)  
- **Instructions:** Download the CSV and place it in the `data/` folder before running the analysis.

---

## Automation & Analysis Pipeline
1. **Data Cleaning & Transformation**  
   - Standardized product names, removed duplicates, handled missing values.  
   - Generated derived metrics like **purchase efficiency** and **discount effectiveness**.  

2. **Exploratory Data Analysis (EDA)**  
   - Visualized trends across **price brackets, discounts, and review ratings**.  
   - Identified high-value products and outliers.

3. **Predictive Modeling**  
   - **Linear Regression** to measure influence of price, reviews, and discounts on purchase volume.  
   - **Random Forest** for feature importance and identifying key sales drivers.

---

## Visualizations
- Product popularity vs. review score  
- Discount impact on purchase efficiency  
- Revenue by price bracket and category  
- Feature importance from Random Forest model  

###Tableau Dashboard
**[View Interactive Dashboard →](https://public.tableau.com/app/profile/galen.pike/viz/BusinessProjectPortfolio/Dashboard1#1)**

---

## File Structure
Business-Portfolio-Project/
│
├── data/
│ ├── raw/ # Original e-commerce CSV from Kaggle
│ ├── processed/ # Cleaned and aggregated datasets
│ └── final_dataset.csv # Ready-to-use dataset for analysis
│
├── notebooks/
│ ├── data_cleaning.ipynb # Cleaning and transformation workflow
│ ├── metrics_eda.ipynb # Metric calculation, EDA, and visualization
│ └── modeling.ipynb # Predictive modeling and feature importance
│
├── scripts/
│ └── cleaning_functions.py # Reusable Python functions for data cleaning & aggregation
│
├── visuals/ # Plots, histograms, and model visualizations
└── README.md

Tableau Link: https://public.tableau.com/app/profile/galen.pike/viz/BusinessProjectPortfolio/Dashboard1#1

---

## Results & Insights

### Key Business Findings
- Discounts above **40%** resulted in diminishing returns on total revenue.  
- **20% of products generated 80% of total profit**, highlighting high-value SKUs for targeted promotions.  
- High review scores strongly correlate with **purchase frequency**, indicating the importance of reputation management.

### Predictive Modeling Insights
- **Random Forest** identified **price, review score, and discount percentage** as the top three drivers of purchase volume.  
- Linear regression revealed that moderate discounts **increase purchase likelihood** but aggressive discounts do not proportionally increase revenue.

### Key Takeaway
The project demonstrates a **full data-to-insight workflow**, providing actionable recommendations for **pricing, discount strategy, and product promotion optimization**.

**Dataset:** The dataset used in this project (42k+ transactions) is available on [Kaggle] https://www.kaggle.com/datasets/ikramshah512/amazon-products-sales-dataset-42k-items-2025 Download it and place it in the `data/` folder before running the analysis.
