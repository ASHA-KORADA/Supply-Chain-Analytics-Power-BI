# Supply Chain Analytics | Power BI

## 📌 Project Overview

This project is a **Supply Chain Analytics dashboard developed in Power BI using synthetic data**.

The objective is to transform operational and transactional supply chain data into an interactive analytical solution covering **procurement performance, supplier performance and risk, and logistics & delivery efficiency**.

> **Note:** This project uses synthetic data created for learning and portfolio purposes. The metrics and insights are not representative of any real organization.

---

## 🎯 Business Objectives

- Monitor procurement spend and purchase order performance
- Evaluate supplier quality, delivery performance, and risk
- Analyze Purchase Price Variance (PPV)
- Track On-Time Delivery (OTD) and shipment delays
- Analyze freight cost across transport modes
- Compare carrier performance against SLA targets
- Identify opportunities to improve procurement and logistics efficiency

---

## 🔹 Data Ingestion & Transformation — Power Query

The project uses **11 separate CSV datasets** covering operational and transactional supply chain data.

Key transformation steps included:

- Ingested 11 separate CSV datasets.
- Used **Append** to combine related datasets.
- Used **Merge** to enrich datasets with additional attributes.
- Applied transformations such as **Pivot, duplicate removal, whitespace trimming, and data type validation**.
- Used **Reference queries** to create the required Dimension tables and Fact tables while maintaining a structured query flow.
- Created a dedicated **Dim_Date** table to support time-based analysis.
- Prepared multiple date relationships for **Order, Dispatch, Promised, and Actual Delivery** dates.

---

## 🔹 Data Modeling — Galaxy Schema

The data model follows a **Galaxy Schema (Fact Constellation)** approach because the project contains multiple fact tables sharing common dimensions.

### Fact Tables

- `Fact_Procurement`
- `Fact_Procurement_Targets`

### Shared Dimensions

- `Dim_Date`
- `Dim_Category`

### Dedicated Dimensions

- `Dim_Product`
- `Dim_Supplier`
- `Dim_Carrier`
- `Dim_Buyer`
- `Dim_Warehouse`

### Role-Playing Dates

The `Dim_Date` table supports multiple date contexts:

- **Order Date** — Active relationship
- **Dispatch Date** — Inactive relationship
- **Promised Date** — Inactive relationship
- **Actual Delivery Date** — Inactive relationship

This structure allows the same Date dimension to support different stages of the procurement and delivery lifecycle.

### Data Model

![Supply Chain Data Model](Data%20Model/Data%20Model-Galaxy%20Schema.png)

---

# 📊 Dashboard

## 1. Home — Landing Page

The landing page provides an introduction to the dashboard and guides users to the three main analytical areas:

- Overview
- Supplier & Procurement Performance
- Logistics & Delivery Performance

![Home - Landing Page](DashBoard%20ScreenShots/Home-Landing%20Page.png)

---

## 2. Overview

Provides a consolidated view of supply chain performance through:

- Procurement Spend vs Target
- Purchase Order Status
- Supplier Risk Profile
- On-Time Delivery
- Average Lead Time
- Rejection Rate
- Spend Variance
- Delivery Delay Analysis

![Overview](DashBoard%20ScreenShots/Page%20-1%20Overview.png)

---

## 3. Supplier & Procurement Performance

Focuses on supplier effectiveness and procurement cost performance through:

- Supplier Quality Score
- Supplier Delivery Score
- Purchase Price Variance (PPV)
- Supplier Spend
- Spend Variance
- Supplier Risk Distribution
- Procurement Performance

![Supplier & Procurement Performance](DashBoard%20ScreenShots/Page%20-2%20Supplier%20%26%20Procurement%20Performance.png)

---

## 4. Logistics & Delivery Performance

Analyzes transportation and delivery efficiency through:

- On-Time Delivery (OTD)
- Freight Cost by Transport Mode
- Transit Time
- Carrier OTD vs SLA Target
- OTD by Region
- Shipment Delays
- Average Transit Time by Carrier

![Logistics & Delivery Performance](DashBoard%20ScreenShots/Page%20-3%20Logistics%20%26%20Delivery%20Performance.png)

---

## 🔍 Key Business Insights

- **₹991.9M** procurement spend, approximately **₹18M below target**.
- **73% of suppliers** fall under the **Medium Risk** category, highlighting the importance of continuous supplier-risk monitoring.
- **Purchase Price Variance (PPV) is 1.12%**, indicating actual procurement costs are slightly above contracted prices.
- **On-Time Delivery stands at 63.71%**, with **487 delayed shipments**, highlighting an opportunity to improve delivery reliability.
- **Air transport accounts for 51.54% of total freight cost**, making it the largest contributor to transportation spend.
- **Road transport contributes the most to shipment delays**, highlighting the need to closely monitor road shipments and carrier performance.

---

## 🧮 DAX & Analytical Techniques

The project uses DAX measures for KPI calculation, time-based analysis, and business performance evaluation.

Key techniques include:

- `CALCULATE`
- `SUMX`
- `AVERAGEX`
- `DIVIDE`
- `DISTINCTCOUNT`
- `FILTER`
- `DATEADD`
- Time-intelligence calculations
- KPI variance analysis
- Supplier and procurement performance measures
- Delivery and logistics performance measures

---

## 🛠️ Tools & Technologies

| Tool / Technology | Usage |
|---|---|
| **Power BI** | Dashboard development & visualization |
| **Power Query** | Data ingestion & transformation |
| **DAX** | Measures & analytical calculations |
| **Data Modeling** | Galaxy Schema / Fact Constellation |
| **Time Intelligence** | Date-based performance analysis |
| **Data Visualization** | KPI and business performance reporting |

---

## 💡 Business Value

The dashboard provides a consolidated view of **procurement costs, supplier risk, and logistics performance**, helping decision-makers:

- Monitor procurement spending
- Identify supplier risk
- Track procurement price variance
- Evaluate delivery reliability
- Monitor transportation costs
- Identify shipment delay patterns
- Support data-driven supply chain improvement

---

## 📁 Repository Structure

```text
Supply-Chain-Analytics/
│
├── DashBoard ScreenShots/
│   ├── Home-Landing Page.png
│   ├── Page -1 Overview.png
│   ├── Page -2 Supplier & Procurement Performance.png
│   └── Page -3 Logistics & Delivery Performance.png
│
├── Data Model/
│   └── Data Model-Galaxy Schema.png
│
├── Power BI/
│   └── Supply Chain Analytics.pbix
│
└── README.md

## 📌 Project Highlights

**Domain:** Supply Chain Analytics  
**Data:** Synthetic  
**Source Datasets:** 11 CSV files  
**Fact Tables:** 2  
**Data Model:** Galaxy Schema / Fact Constellation  
**Dashboard Pages:** 4  
**Tool:** Microsoft Power BI

---

## 📬 Feedback

I welcome feedback on the **dashboard design, data modeling, business insights, and overall analytical approach**.
