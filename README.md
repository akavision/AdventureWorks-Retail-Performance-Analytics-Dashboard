# 🚴 AdventureWorks Retail Performance Analytics Dashboard

A multi-page, interactive Power BI dashboard built to analyze the retail performance of AdventureWorks Bike Shop — covering $25M in revenue, $10.5M in profit, 25K+ orders, and customer-level insights across global markets.

---

## 📌 Short Description / Purpose

The AdventureWorks Retail Performance Analytics Dashboard is a professionally designed, 4-page Power BI report built to help business stakeholders explore sales performance, product trends, customer behavior, and regional distribution. The dashboard tracks key retail KPIs including revenue, profit, return rates, and order volumes — with drill-through capability, dynamic product metric selection, and geo-mapped territory analysis. It is intended for use by retail analysts, business intelligence professionals, sales managers, and data-driven decision makers who want a comprehensive view of business performance.

---

## 🛠️ Tech Stack

The dashboard was built using the following tools and technologies:

- 📊 **Power BI Desktop** – Main data visualization platform used for all 4 report pages.
- 📂 **Power Query** – Data transformation and cleaning layer for reshaping raw sales, returns, and customer data.
- 🧠 **DAX (Data Analysis Expressions)** – Used for 35+ calculated measures including YoY %, Rolling Averages, Return Rate, Revenue per Customer, Target Variance, Adjusted Profit, YTD Revenue, Weekend Orders, and more.
- 📅 **Calendar Lookup Table** – A custom date dimension with Date, Day Name, Day of Week, Month, Month Name, Month Number, Month Short, Start of Month, Start of Quarter, Start of Year, and Weekend flag.
- 🔢 **What-If Parameter** – Price Adjustment (%) parameter enabling dynamic profit scenario modelling.
- 🗺️ **Bing Maps Integration** – Geo-mapped territory analysis across Europe, North America, and Pacific regions.
- 📁 **File Format** – `.pbix` for development; `.png` for dashboard previews.

---

## 📂 Data Source

Source: AdventureWorks sample dataset (Microsoft / Maven Analytics)

The data model follows a **Star Schema** with 2 fact tables and 6 dimension tables:

**Sales Data** (Fact Table)
- `CustomerKey`, `OrderDate`, `OrderLineItem`, `OrderNumber`
- `OrderQuantity`, `ProductKey`, `StockDate`, `TerritoryKey`, `Quantity Type`

**Returns Data** (Fact Table)
- `ProductKey`, `ReturnDate`, `ReturnQuantity`, `TerritoryKey`

**Product Lookup** (Dimension)
- `Discount Price`, `ModelName`, `ProductColor`, `ProductCost`
- `ProductDescription`, `ProductKey`, `ProductName`, `ProductPrice`, `ProductSKU`

**Product Subcategories Lookup** (Dimension)
- `ProductSubcategoryKey`, `SubcategoryName`

**Product Categories Lookup** (Dimension)
- `CategoryName`, `ProductCategoryKey`

**Customer Lookup** (Dimension)
- `AnnualIncome`, `BirthYear`, `BirthDate`, `Customer Full Name (CC)`, `Customer Priority`
- `CustomerKey`, `Domain Name`, `Education Category`, `EducationLevel`
- `EmailAddress`, `FirstName`, `LastName`, `Full Name`, `Gender`
- `HomeOwner`, `Income Level`, `Is Parent?`

**Territory Lookup** (Dimension)
- `Continent`, `Country`, `Region`, `SalesTerritoryKey`

**Calendar Lookup** (Date Dimension)
- `Date`, `Day Name`, `Day of Week`, `Month`, `Month Name`
- `Month Number (DAX)`, `Month Short`, `Start of Month`, `Start of Quarter`, `Start of Year`, `Weekend`

**Measure Table** – A dedicated table housing all 35+ DAX measures for clean model organization.

---

## ✨ Features / Highlights

### 🔴 Business Problem

Retail businesses like AdventureWorks generate enormous volumes of sales, returns, and customer data — but without a unified analytical tool, it's difficult to answer critical questions such as:

- Which products and categories drive the most revenue and profit?
- Which customers contribute the most value?
- Where are return rates unusually high, signaling product or quality issues?
- How does performance compare against monthly targets?
- Which regions and territories are growing or underperforming?

Raw transactional data across multiple tables makes these insights inaccessible without proper modeling and visualization.

---

### 🎯 Goal of the Dashboard

To deliver a comprehensive, 4-page interactive business intelligence tool that:

- Provides an executive summary of overall retail performance at a glance.
- Enables product-level drill-through analysis with dynamic metric switching.
- Identifies high-value customers and segments by income, occupation, and geography.
- Supports pricing scenario analysis through a What-If price adjustment parameter.
- Tracks performance against monthly order, revenue, and profit targets.

---

### 📊 Walkthrough of Key Visuals

**Page 1 — Executive Summary**

**🔢 Top KPI Cards**
- **Revenue:** $24.9M
- **Profit:** $10.5M
- **Total Orders:** 25.2K
- **Return Rate:** 2.2%

**📈 Yearly Revenue (Line Chart)**
Revenue trend from 2020 to 2022, showing consistent growth with a strong upward trajectory into 2022.

**📊 Monthly KPI Cards with MoM Comparison**
- Monthly Revenue: $1.59M (vs Prev Month $1.47M, +7.62%)
- Monthly Orders: 1.84K (vs Prev Month 1.79K, +2.57%)
- Monthly Returns: 150 (vs Prev Month 148, +1.35%)

**📊 Orders by Category (Bar Chart)**
- Accessories: 17K orders
- Bikes: 13.9K orders
- Clothing: 7K orders

**📋 Top 10 Products Table**
Ranked by orders, revenue, and return % — Sport-100 Helmet (Red & Blue) show the highest return rates at 3.31% and 3.33% respectively.

**🏷️ Most Ordered / Most Returned Product Type**
- Most Ordered: Tires and Tubes
- Most Returned: Shorts

---

**Page 2 — Map & Territory View**

**🗺️ Geographic Revenue Map**
Interactive map with continent filter buttons (Europe, North America, Pacific). Bubble markers show revenue concentration by region, with drill-down to country level.

---

**Page 3 — Product Detail**

**🎯 Monthly vs Target Gauges**
Three gauge charts tracking selected product performance against targets:
- Monthly Orders vs Target
- Monthly Revenue vs Target
- Monthly Profit vs Target

**📈 Total Profit vs Adjusted Profit (Line Chart)**
Dual-line chart comparing actual profit against price-adjusted profit using the What-If parameter (Price Adjustment % slider).

**📉 Yearly Returns (Area Chart)**
Daily return volume trend across Jul 2021 – Jun 2022.

**🔘 Product Metric Selection**
Radio button slicer to switch the main chart metric between Orders, Revenue, Profit, Returns, and Return %.

---

**Page 4 — Customer Detail**

**🔢 Customer KPIs**
- Unique Customers: 17.4K
- Revenue per Customer: $1.4K

**📈 Total Customers & Revenue Per Customer (Line Chart)**
Trend from Jan 2020 to Jan 2022 showing customer growth over time.

**🍩 Orders by Income Level**
- Average: 11.6K
- Low: 10.3K
- High: 2.8K

**🍩 Orders by Occupation**
- Professional: 7.9K
- Skilled Manual: 6.0K
- Management: 4.4K
- Clerical: 4.0K
- Manual: 2.9K

**📋 Top 100 Customers Table**
Full customer ranking by orders and revenue with drill-through capability.

**🏆 Top Customer Spotlight**
- Top Customer: **Mr. Maurice Shan**
- Orders: 6 | Revenue: $12.4K

---

### 💡 Business Impact & Insights

- **Revenue Growth:** Consistent YoY revenue growth reaching $24.9M total, with monthly revenue up 7.62% — signaling strong business momentum.
- **High-Return Products:** Sport-100 Helmets show return rates above 3%, flagging potential quality or sizing issues that warrant product review.
- **Customer Value Concentration:** Top customers like Mr. Maurice Shan generate $12K+ from just 6 orders, highlighting the importance of high-value customer retention strategies.
- **Category Focus:** Accessories lead in order volume (17K) but Bikes likely drive higher revenue per unit — supporting category-specific pricing and marketing strategies.
- **Pricing Scenario Planning:** The What-If price adjustment parameter enables instant profit impact modelling without changing underlying data.
- **Geographic Expansion:** Territory map enables region-by-region performance comparison across Europe, North America, and Pacific markets.

---

## 📸 Dashboard Preview

![Executive Summary](https://raw.githubusercontent.com/akavision/AdventureWorks-Retail-Performance-Analytics-Dashboard/main/Snapshot%20of%20Dashboard1.png)

![Map View](https://raw.githubusercontent.com/akavision/AdventureWorks-Retail-Performance-Analytics-Dashboard/main/Snapshot%20of%20Dashboard2.png)

![Product Detail](https://raw.githubusercontent.com/akavision/AdventureWorks-Retail-Performance-Analytics-Dashboard/main/Snapshot%20of%20Dashboard3.png)

![Customer Detail](https://raw.githubusercontent.com/akavision/AdventureWorks-Retail-Performance-Analytics-Dashboard/main/Snapshot%20of%20Dashboard4.png)

---

## 🚀 How to Use

1. Download and open `AdventureWorks.pbix` in **Power BI Desktop**.
2. Navigate between the 4 report pages using the left sidebar icons.
3. Use the **continent filter buttons** on the Map page to filter by region.
4. Select any product on the Executive Summary to drill through to the **Product Detail** page.
5. Use the **Price Adjustment (%) slider** to model profit scenarios dynamically.
6. Switch between metrics using the **Product Metric Selection** radio buttons.
7. Filter the Customer Detail page by **Year slicer** to analyze customer trends over time.

---

*Built by Akhilesh Madwalkar | Power BI | DAX | Data Analytics*
