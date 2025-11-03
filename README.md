# Workout Progress Analytics

**Version:** Iterative Development | **Tools:** Python, Pandas, Tableau

---

## Overview
This project analyzes **three years of personal workout data (2022–2025)** to measure long-term strength and volume progression across all major muscle groups.  
It demonstrates a **complete data analytics workflow** — from raw data transformation and feature engineering to visualization and performance analysis.

---

## Objectives
- Engineer multiple training metric tables and merge them into a unified analytical dataset.  
- Track **strength and volume progression** across key muscle groups.  
- Identify **peak performance periods** and **training plateaus**.  
- Visualize **8-week block progressions** for smarter periodization insights.

---

## Tech Stack
| Category | Tools / Libraries |
|-----------|-------------------|
| **Language** | Python |
| **Libraries** | Pandas, NumPy, Matplotlib, Seaborn |
| **Tools** | Jupyter Notebook, VS Code, Google Colab |
| **Visualization** | Tableau |
| **Workflow** | Automated ETL Pipeline (Extract → Transform → Merge → Analyze) |

---

## Dataset Engineering
Two original datasets (2022–2023 and 2024–2025) were processed to generate four derived metric tables:

| Table | Purpose | Columns (9 total) |
|--------|----------|------------------|
| **Total_Load** | Tracks cumulative load per session | Chest, Upper Back, Triceps, Lats, Traps, Biceps, Quads, Hamstrings, Calves |
| **Total_Sets** | Total number of sets per muscle group | Same 9 columns |
| **Total_Reps** | Total repetitions performed | Same 9 columns |
| **Weight_Per_Rep** | Average weight lifted per repetition | Same 9 columns |

After cleaning and normalization, all tables were merged into one **master analytical dataset** for visualization and analysis.

---

## Automation Pipeline
A custom **automation script** streamlines the entire ETL process:

- Dynamically reads and renames raw workout files.  
- Cleans, standardizes, and aggregates per metric type.  
- Outputs intermediate and final datasets for Tableau visualization.

**Example Snippet:**
```python
# Automatically rename weeks into structured blocks
df = auto_rename_weeks(df)
df2024 = auto_rename_weeks(df2024, block_sizes=[8,8,8,8,4])

# Create metric tables for all muscles
tables_2022 = create_metric_table(df, muscles_2022)
tables_2024 = create_metric_table(df2024, muscles_2024)

# Merge datasets automatically
merged = {
    metric: pd.concat(
        [prepare_metric_table(tables_2022, metric),
         prepare_metric_table(tables_2024, metric)],
        ignore_index=True
    )
    for metric in metrics
}
```
## 🧾 File Structure
/Workout-Progress-Analysis
│
├── data/
│   ├── raw/                     # Original input CSV files (2022–2023.csv, 2024–2025.csv)
│   ├── processed/               # Generated metric tables (Total Load, Sets, Reps, Weight Per Rep)
│   └── merged_dataset.csv       # Final merged dataset for analysis
│
├── notebooks/
│   ├── automation_pipeline.ipynb       # Full ETL workflow and metric table creation
│   ├── analysis_visualization.ipynb    # Exploratory data analysis, plots, and trends
│
├── scripts/
│   └── automate_metrics.py             # Python functions for automated data cleaning & table generation
│
├── visuals/                             # Exported charts, histograms, and heatmaps
│
└── README.md                            # Project documentation


Link for Tableau: (https://public.tableau.com/views/WorkoutSheet/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)(https://public.tableau.com/views/WorkoutAnalyticsVisualization/WorkoutProgressDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## 📈 Results & Insights

### Training Progression
- **Overall strength increased by 22%** over three years, measured by total load volume.  
- **Upper body muscles (Chest, Lats, Triceps)** showed the most consistent volume growth.  
- **Leg-focused work (Quads, Hamstrings)** improved in total load but fluctuated due to training block cycles.

### Periodization Insights
- Most significant growth occurred during **Weeks 9–16 and 33–40**, aligning with structured progression blocks.  
- Strength plateaus appeared between **Weeks 17–24**, suggesting overreach or recovery phases.

### Load Distribution
- Balanced training distribution across all nine muscle groups.  
- **Traps and Biceps** remained stable but undertrained relative to larger muscle groups — an insight for program adjustment.

### Key Takeaway
The automated ETL workflow successfully quantified **real-world performance trends**, transforming raw training logs into a reproducible analytical dataset and visualization pipeline — the same workflow structure used in professional analytics environments.
