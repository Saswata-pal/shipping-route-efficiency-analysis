# 🚚 Factory-to-Customer Shipping Route Efficiency Analysis

An end-to-end logistics analytics project that transforms raw shipment records into actionable route-level intelligence for Nassau Candy, a specialty confections distributor. The project cleans and engineers features from raw shipment data, benchmarks route and shipping-mode efficiency, and surfaces the results in an interactive Streamlit dashboard for decision-makers.

Built as part of a Data Analyst Internship with **Unified Mentor Pvt. Ltd.**

---

## 🔗 Live Demo

**Dashboard:** [[click here](https://shipping-route-efficiency-analysis-cww.streamlit.app/)]

**Repository:** https://github.com/Saswata-pal/shipping-route-efficiency-analysis

---

## 📌 Project Overview

Efficient logistics is essential for improving customer satisfaction, reducing operational costs, and scaling nationwide distribution networks. This project evaluates shipping route efficiency by analyzing shipment lead times between Nassau Candy's manufacturing factories and customer locations across the US.

The pipeline moves from raw order-level data through cleaning, feature engineering, and route-level aggregation, into a normalized **Route Efficiency Score**, and finally into a filterable, multi-tab dashboard covering route benchmarking, geographic bottlenecks, ship-mode comparison, route drill-down, and monthly trends.

---

## 🎯 Objectives

- Analyze shipping lead times across factory-to-customer routes
- Identify the fastest and slowest shipping routes
- Detect regional and state-level logistics bottlenecks
- Compare shipping performance across different shipping modes
- Measure operational efficiency using a normalized Route Efficiency Score
- Build an interactive dashboard for business users, with both desktop and mobile-friendly filtering

---

## 📊 Dataset

Source: `data/Nassau Candy Distributor.csv`

The dataset contains order-level shipment records including:

- Order ID, Order Date, Ship Date
- Factory (origin) and Customer State/Province, Region (destination)
- Ship Mode
- Derived: Shipping Lead Time, Route (Factory → State / Factory → Region), Delay Status

Cleaned and feature-engineered versions are exported to `data/processed/` for the dashboard, and to `data/powerbi_ready/` for use outside Streamlit (e.g. Power BI).

---

## ⚙️ Project Workflow

```
Raw Dataset (Nassau Candy Distributor.csv)
      │
      ▼
Data Cleaning & Validation
      │
      ▼
Feature Engineering
      │
      ▼
Route Definition & Aggregation
      │
      ▼
Efficiency Benchmarking (Route Efficiency Score)
      │
      ▼
Geographic Bottleneck Analysis
      │
      ▼
Ship Mode Performance Analysis
      │
      ▼
Export for Streamlit + Power BI
      │
      ▼
Interactive Streamlit Dashboard
      │
      ▼
Key Insights & Recommendations
```

The full pipeline is documented step-by-step in `notebooks/01` through `notebooks/09`.

---

## 📈 Key Performance Indicators

- Shipping Lead Time (median) and Average Lead Time (mean)
- Route Volume (average shipments per route)
- Delay Frequency (% shipments above a configurable lead-time threshold)
- Route Efficiency Score (normalized, 0–100, higher is faster/better)
- Total Shipments, Unique Orders, Avg Shipments per Order

---

## 📊 Dashboard Features

The dashboard (`app/app.py`) is organized into five tabs, plus a persistent KPI header and a synced filter panel (sidebar on desktop, expander on mobile) for date range, region/state, ship mode, and delay-threshold filtering.

### Route Overview
- Route efficiency bar chart and volume-vs-lead-time scatter plot
- Top 10 / Bottom 10 efficient routes leaderboard
- Full route performance leaderboard table

### Geographic View
- US choropleth map of state-level average lead time
- Regional bottleneck bar chart
- Bottleneck state detection (top 25% volume + top 25% lead time)

### Ship Mode Analysis
- Lead time comparison across shipping modes
- Delayed vs. on-time percentage by ship mode
- Best/slowest mode summary cards

### Route Drill-Down
- Per-route order timeline (on-time vs. delayed shipments)
- Full order-level record table for the selected route
- Analyst recommendation based on that route's performance vs. the overall average

### Trends
- Monthly average lead time and order volume trends
- Month-over-month movement summaries
- Peak/lowest volume and lead-time months, with analyst recommendations

Insights and recommendations throughout the dashboard are generated dynamically from the currently filtered data, not hardcoded.

---

## 📂 Actual Project Structure

```
nassau-candy-shipping-route-efficiency-analysis/
│
├── app/
│   ├── app.py                          # Streamlit dashboard
│   ├── powerbi_ready_dataset_builder.py
│   ├── prepare_dashboard_files.py
│   └── assets/
│       ├── nassau_shippingrouteanalysis.css
│       └── images/
│
├── data/
│   ├── Nassau Candy Distributor.csv    # raw source data
│   ├── *.csv                           # intermediate analysis exports
│   ├── processed/                      # cleaned data consumed by app.py
│   └── powerbi_ready/                  # exports for Power BI
│
├── notebooks/
│   ├── 01_project_overview_and_data_loading.ipynb
│   ├── 02_data_cleaning_and_validation.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_route_definition_and_aggregation.ipynb
│   ├── 05_efficiency_benchmarking.ipynb
│   ├── 06_geographic_bottleneck_analysis.ipynb
│   ├── 07_ship_mode_performance_analysis.ipynb
│   ├── 08_key_insights_and_recommendations.ipynb
│   └── 09_export_cleaned_data_for_streamlit.ipynb
│
├── reports/
├── requirements.txt
├── Project Guidelines.txt
└── README.md
```

---

## 🛠️ Tech Stack

- **Language:** Python
- **Data Processing:** Pandas, NumPy
- **Visualization:** Plotly (Express & Graph Objects)
- **Dashboard:** Streamlit, with a custom CSS theme (`app/assets/nassau_shippingrouteanalysis.css`)

---

## ▶️ Running Locally

```bash
git clone https://github.com/Saswata-pal/shipping-route-efficiency-analysis.git
cd shipping-route-efficiency-analysis
pip install -r requirements.txt
streamlit run app/app.py
```

The app expects the processed CSVs in `data/processed/`; regenerate them from the raw dataset via the notebooks in `notebooks/` (or `app/prepare_dashboard_files.py`) if they're not already present.

---

## ☁️ Deployment

Deployed via **Streamlit Community Cloud**, pointed at `app/app.py` as the main file. Pushing to the connected branch auto-redeploys.

---

## 📌 Key Insights Answered

- Which factory-to-state routes are the fastest and slowest?
- Which regions and states show the highest delay frequency?
- Which shipping mode delivers most reliably, and which is used too often for its performance?
- Which states are volume + lead-time bottlenecks that need operational review?
- How has shipping performance trended month over month?

---

## 🚀 Future Enhancements

- Route delay prediction using Machine Learning
- Route optimization recommendations
- Interactive route maps with factory-to-customer paths
- Automated report generation
- Cost vs. lead-time trade-off analysis
- Real-time logistics monitoring

---

## 📄 License

This project is intended for educational, research, and portfolio purposes.

---

## 👨‍💻 Author

**Saswata Pal**
Machine Learning Intern — Unified Mentor Pvt. Ltd.

**GitHub:** https://github.com/Saswata-pal