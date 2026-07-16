# 🚚 Factory-to-Customer Shipping Route Efficiency Analysis

An end-to-end logistics analytics project that transforms raw shipment records into actionable route-level intelligence. This project analyzes factory-to-customer shipping performance, identifies logistics bottlenecks, compares shipping modes, and provides an interactive Streamlit dashboard for decision-makers.

---

## 📌 Project Overview

Efficient logistics is essential for improving customer satisfaction, reducing operational costs, and scaling nationwide distribution networks. This project focuses on evaluating shipping route efficiency by analyzing shipment lead times between manufacturing factories and customer locations.

Using data analytics, geospatial visualization, and business intelligence techniques, the project helps identify high-performing shipping routes, detect geographical bottlenecks, and compare shipping methods across different regions.

---

## 🎯 Objectives

- Analyze shipping lead times across factory-to-customer routes
- Identify the fastest and slowest shipping routes
- Detect regional logistics bottlenecks
- Compare shipping performance across different shipping modes
- Measure operational efficiency using logistics KPIs
- Build an interactive dashboard for business users

---

## 📊 Dataset

The dataset contains information about:

- Orders
- Shipment dates
- Customer locations
- Product information
- Factory mappings
- Sales
- Cost
- Gross Profit
- Units Sold
- Shipping Mode

Additional lookup tables map products to factories and factory geographic coordinates.

---

## ⚙️ Project Workflow

```
Raw Dataset
      │
      ▼
Data Cleaning
      │
      ▼
Feature Engineering
      │
      ▼
Route Definition
      │
      ▼
KPI Calculation
      │
      ▼
Exploratory Data Analysis
      │
      ▼
Geospatial Analytics
      │
      ▼
Interactive Streamlit Dashboard
      │
      ▼
Business Insights & Recommendations
```

---

## 📈 Key Performance Indicators

- Shipping Lead Time
- Average Lead Time
- Route Volume
- Route Efficiency Score
- Delay Frequency
- Average Sales
- Gross Profit
- Units Shipped
- Factory Performance
- Regional Performance

---

## 📊 Dashboard Features

### Executive Dashboard

- Overall KPIs
- Shipment Summary
- Route Efficiency Score
- Factory Performance

### Route Analytics

- Route Leaderboard
- Fastest Routes
- Slowest Routes
- Route Performance Comparison

### Geographic Analytics

- Factory Locations
- Customer Distribution
- US Shipping Heatmap
- Regional Bottlenecks

### Ship Mode Analytics

- Lead Time Comparison
- Shipment Distribution
- Cost vs Time Analysis

### Factory Analytics

- Factory Performance
- Orders by Factory
- Product Distribution

### State Drill-down

- State-wise Performance
- Shipping Timeline
- Order Details

---

## 📂 Proposed Project Structure

```
shipping-route-efficiency-analysis/
│
├── data/
│   ├── raw/
│   ├── processed/
│   ├── external/
│
├── notebooks/
│
├── src/
│   ├── preprocessing/
│   ├── feature_engineering/
│   ├── visualization/
│   ├── analytics/
│   ├── utils/
│
├── dashboard/
│   ├── pages/
│   ├── components/
│   ├── assets/
│
├── reports/
│
├── models/
│
├── requirements.txt
├── app.py
├── README.md
└── LICENSE
```

---

## 🛠️ Tech Stack

### Programming

- Python

### Data Processing

- Pandas
- NumPy

### Visualization

- Plotly
- Matplotlib
- Folium

### Dashboard

- Streamlit

### Geospatial Analytics

- GeoPandas
- Geopy

### Machine Learning (Optional)

- Scikit-learn

---

## 📌 Expected Insights

The project aims to answer questions such as:

- Which factory delivers products most efficiently?
- Which customer regions experience the highest delays?
- Which shipping mode provides the best performance?
- Which routes require operational optimization?
- How does shipment performance vary geographically?

---

## 🚀 Future Enhancements

- Route delay prediction using Machine Learning
- Route optimization recommendations
- Interactive route maps
- Automated report generation
- Forecasting shipment demand
- Cost optimization analysis
- Real-time logistics monitoring

---

## 📄 License

This project is intended for educational, research, and portfolio purposes.

---

## 👨‍💻 Author

Developed as a data analytics and business intelligence project demonstrating logistics optimization, geospatial analytics, and interactive dashboard development.