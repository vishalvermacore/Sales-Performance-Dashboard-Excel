# 📊 RetailPulse — Excel Sales Performance Dashboard

**An interactive, slicer-driven Excel dashboard built entirely with PivotTables, PivotCharts, and native Excel features — no add-ins, no macros.**

![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Type](https://img.shields.io/badge/Type-Portfolio%20Project-blue)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📌 Overview

This project simulates a real-world business ask: **a sales manager needs a single, clean view of performance** instead of scrolling through thousands of raw order rows or flipping between multiple PivotTables.

The result is a **one-page interactive Sales Dashboard** built on 2,000 order-level transaction records, covering FY2026, that lets a non-technical stakeholder filter, explore, and read key sales metrics in seconds.

> **Goal:** Turn raw transactional data into a decision-ready dashboard using only core Excel functionality — PivotTables, PivotCharts, Slicers, and Timelines.

---

## 🧠 Business Problem

| Challenge | Solution |
|---|---|
| Manager can't quickly assess sales health | Central KPI cards for Revenue, Orders, Quantity, AOV |
| No visibility into trends over time | Monthly revenue trend chart + Timeline filter |
| Hard to compare regions, channels, categories | Dedicated PivotCharts per dimension |
| Multiple disconnected PivotTables to check manually | One unified, filterable dashboard view |
| Risk of accidental edits when shared | Protected dashboard sheet with interaction-only access |

---

## 🗂️ Dataset

The dataset contains **2,000 order-level sales records** for the 2026 fiscal year.

| Field | Description |
|---|---|
| `Order ID` | Unique identifier per transaction |
| `Date` | Order date (Jan – Dec 2026) |
| `Region` | North, South, East, West, Central |
| `Sales Channel` | Online, Retail Store, Marketplace, Corporate Sales |
| `Customer Type` | New / Returning |
| `Product Category` | Computers, Monitors, Networking, Storage, Accessories, Office Supplies |
| `Product` | Individual product name |
| `Salesperson` | Sales rep assigned to the order |
| `Quantity` | Units sold |
| `Unit Price` | Price per unit |
| `Discount` | Discount rate applied |
| `Revenue` | Final order revenue (post-discount) |

**Data quality checks performed:** verified headers, confirmed dates recognized as true date values (not text), validated numeric fields, standardized categorical labels, and converted the range into a structured **Excel Table** to keep PivotTables dynamic as new rows are added.

---

## 🏗️ Project Workflow

```
Raw Data → Excel Table → Dashboard Plan → PivotTables → PivotCharts → Slicers/Timeline → Layout & Formatting → Sheet Protection
```

1. **Reviewed the raw data** — confirmed structure, one row per order, no blank/duplicate headers, correct data types.
2. **Converted the range to an Excel Table** — for a self-expanding, structured data source.
3. **Planned the dashboard** — mapped every business requirement to a specific dashboard element *before* touching PivotTables (see plan below).
4. **Built supporting PivotTables** — one PivotTable per KPI/chart, kept on a separate `Supporting_Pivot` sheet.
5. **Created PivotCharts** — visual layer on top of each PivotTable.
6. **Added Slicers & Timeline** — for Region, Product Category, Sales Channel, Customer Type, and Date (Year/Quarter/Month).
7. **Designed the dashboard layout** — header, KPI cards, charts, slicers, arranged for a clean single-screen view.
8. **Protected the dashboard sheet** — end users can filter via slicers/timeline without being able to move or break the layout.

---

## 📋 Dashboard Plan

| Requirement | Dashboard Element | Fields Used |
|---|---|---|
| Total Revenue | KPI Card | `Revenue` |
| Total Orders | KPI Card | `Order ID` |
| Quantity Sold | KPI Card | `Quantity` |
| Average Order Value | KPI Card | `Revenue`, `Order ID` |
| Monthly Revenue Trend | Line/Column PivotChart | `Date`, `Revenue` |
| Regional Performance | PivotChart | `Region`, `Revenue` |
| Product Category Performance | PivotChart | `Product Category`, `Revenue` |
| Sales Channel Contribution | PivotChart | `Sales Channel`, `Revenue` |
| Top Products by Revenue | Top 5 PivotChart | `Product`, `Revenue` |

---

## 📈 Key Metrics (FY2026 Snapshot)

| Metric | Value |
|---|---|
| **Total Revenue** | ₹ 24,52,084 (~2.45M) |
| **Total Orders** | 2,000 |
| **Total Quantity Sold** | 5,552 units |
| **Average Order Value** | ₹ 1,226 |
| **Regions Covered** | North, South, East, West, Central |
| **Sales Channels** | Online, Retail Store, Marketplace, Corporate Sales |
| **Product Categories** | Computers, Monitors, Networking, Storage, Accessories, Office Supplies |

*(Adjust currency symbol/values above if your dataset uses a different currency.)*

---

## 🖥️ Dashboard Preview

> Add a screenshot of your final `Sales_Dashboard` sheet here for maximum impact.

```
[ Insert dashboard-screenshot.png here ]
```

---

## 🧰 Tools & Features Used

- Microsoft Excel (Tables, PivotTables, PivotCharts)
- Slicers (Region, Category, Channel, Customer Type)
- Timeline filter (Year / Quarter / Month / Date)
- Worksheet protection for a share-safe, interactive view
- Native formatting only — **no VBA, no macros, no external add-ins**

---

## 📁 Repository Structure

| Sheet | Purpose |
|---|---|
| `Start_Here` | Quick guide to navigating the workbook |
| `Dashboard_Plan` | Requirement → element → field mapping |
| `Sales_Data` | Raw, table-formatted sales dataset (2,000 rows) |
| `Supporting_Pivot` | All PivotTables powering the dashboard |
| `Sales_Dashboard` | Final interactive, protected dashboard |

```
📦 retailpulse-excel-dashboard
 ┣ 📊 Sales_Data.xlsx                  # Full workbook with data + dashboard
 ┣ 📊 Excel_Dashboard_Practice.xlsx    # Practice/working copy
 ┗ 📄 README.md
```

---

## 🔑 Key Takeaways

- Always audit and clean raw data before building any PivotTable-based reporting.
- A written dashboard plan (requirement → element → fields) prevents scope creep and keeps charts purposeful.
- PivotTables should sit on a hidden/supporting sheet — never build charts directly off raw data.
- Sheet protection is essential before sharing a dashboard so slicers/timelines stay usable but the layout stays intact.
- Test every slicer and timeline interaction **after** protecting the sheet, not before.

---

## 🚀 How to Use

1. Download `Sales_Data.xlsx`.
2. Open the `Sales_Dashboard` sheet.
3. Use the **slicers** (Region, Category, Channel, Customer Type) and **timeline** (Date) to filter the view.
4. KPI cards and charts update instantly based on your selections.

---

## 👤 Author

**[Your Name]**
Data Analyst | Excel • Power BI • SQL
📧 [your-email@example.com] | 🔗 [LinkedIn](#) | 🔗 [Portfolio](#)

---

## 📝 License

This project is released under the [MIT License](LICENSE) — free to use for learning and portfolio purposes.
