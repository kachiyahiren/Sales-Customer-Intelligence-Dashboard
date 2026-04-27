📊 Sales & Customer Intelligence Dashboard (Power BI)

## 🚀 Project Overview
This project is an interactive **Power BI dashboard** designed to analyze sales performance and customer behavior across multiple dimensions such as time, region, product, and category.

It enables businesses to track KPIs, identify trends, and make data-driven decisions using visual storytelling.

---

## 🎯 Business Objectives
- Monitor overall sales performance and growth
- Identify top-performing regions and categories
- Analyze customer-level sales contribution
- Track yearly sales trends and returns
- Enable drill-down analysis for deeper insights

---

## 📊 Dashboard Structure

### 🟢 Main Dashboard
Provides a high-level overview of business performance.

#### Key Highlights:
- 💰 **Total Sales:** ₹844.02K
- 📦 **Total Orders:** 1000
- 📈 **Growth Rate:** 5.00%

#### Visuals Included:
- 📉 Sales Trend (Year-Month Analysis)
- 🌍 Sales by Region (South, North, West, East)
- 🧾 Product-Level Performance Table
- 🍩 Category Contribution (Donut Chart)
- 🎯 Category Filters (Furniture, Office Supplies, Technology)

---

### 🔵 Detail Page
Focused on granular, customer-level insights.

#### Key Features:
- 👤 Customer-wise Sales Analysis
- 📅 Year-wise Comparison (2024 vs 2025)
- 🔄 Returns Tracking
- 📊 Conditional Formatting (Performance Heatmap)
- 🌍 Region Filters for targeted analysis

---

## 📌 Key Insights
- **South region** is the top revenue contributor
- **Office Supplies** leads in category sales
- Sales show a **declining trend over months**, indicating possible seasonality or performance issues
- Certain customers contribute significantly more revenue → potential for targeted marketing
- Returns are relatively low but visible across both years

---

## 🛠️ Tools & Technologies
- **Power BI Desktop**
- Power Query (Data Transformation)
- DAX (Data Analysis Expressions)
- Data Modeling (Relationships, Star Schema)

---

## ⚙️ Data Modeling Approach
- Created relationships between:
  - Sales Table
  - Customer Table
  - Product Table
  - Date Dimension
- Used **Date Table** for time intelligence calculations
- Applied **measures for KPIs** instead of calculated columns


## SCREENSHORT
MAIN DASHBOARD: https://github.com/kachiyahiren/Sales-Customer-Intelligence-Dashboard/blob/main/MAIN%20DASHBOARD.png

DETAIL PAGE DASHBOARD: https://github.com/kachiyahiren/Sales-Customer-Intelligence-Dashboard/blob/main/DETAIL%20PAGE%20DASHBOARD.png


---

## 🧮 Key DAX Measures (Examples)

```DAX
Total Sales = SUM(Sales[SalesAmount])

Total Orders = COUNT(Sales[OrderID])

Profit = SUM(Sales[Profit])

YOY Growth % =
DIVIDE(
    [Total Sales] - CALCULATE([Total Sales], SAMEPERIODLASTYEAR(Date[Date])),
    CALCULATE([Total Sales], SAMEPERIODLASTYEAR(Date[Date]))
)
