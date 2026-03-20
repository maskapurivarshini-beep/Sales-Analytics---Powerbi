Chocolate Sales Analytics Platform
End-to-End Power BI Business Intelligence Solution

🎥 Dashboard Walkthrough

Click below to watch the full dashboard demo:

Show Image
🔗 ▶ Watch Full Dashboard Walkthrough on YouTube(https://youtu.be/https://youtu.be/SPh57nZFDu4)

1. Project Overview
This project delivers a full-scale Sales Analytics Dashboard for a
chocolate manufacturing company distributing to bakeries, retail shops,
and distributors across multiple geographies.
Although the current dataset is small (Excel-based), the architecture
was designed following enterprise BI standards so it can scale to
database-level volume (SQL Server / Azure / Snowflake) in future
deployments.

Business Objectives
The company wanted answers to:

Which products generate the most revenue?
Which salespeople are driving profit?
Are we improving year-over-year?
Which teams and regions need performance intervention?
How efficiently are we selling (Amount per Box)?


Data Architecture & Modeling Approach
1. Data Source

Excel-based structured dataset
Multiple tables:

Shipments (Fact Table)
Products
Geography
Salesperson
Calendar



2. Data Modeling
Implemented a Star Schema in Power BI:
Fact Table – Shipments

Shipment_ID
SP_ID (Salesperson)
P_ID (Product)
G_ID (Geo)
Shipment_Date
Amount
Boxes
Order_Status

Dimension Tables

Product Table
Salesperson Table
Geography Table
Calendar Table

Relationships were explicitly defined in Model View to ensure proper filtering, accurate aggregations, and time intelligence functionality.

📊 Sheet 1 - Product Performance by Geography
Business Question: Which products are generating the highest revenue in each country?
Implementation:

Bar Chart: Product vs Total Amount
Slicer: Geo (Country)
Enabled visual interactions for dynamic filtering

DAX Measure:
daxTotal Amount = SUM(Shipments[Amount])
Insights Enabled: Product dominance by country, revenue concentration analysis, geo-based performance segmentation.

📊 Sheet 2 - Profitability Analysis
Business Question: Are we actually profitable? Which markets and products drive profit?
DAX Measures:
daxTotal Amount = SUM(Shipments[Amount])
Total Cost = SUM(Shipments[Cost])
Total Profit = [Total Amount] - [Total Cost]
Profit % = DIVIDE([Total Profit], [Total Amount])
Visuals:

Bar chart comparing Amount vs Cost
Table: Profit by Country
Conditional Formatting: Green → Positive Margin | Red → Negative Margin


📊 Sheet 3 - Shipment Volume & Team Activity
Business Question: Which teams are operationally stronger? Are shipments increasing over time?
DAX Measure:
daxShipment Count = COUNTROWS(Shipments)
Visuals: Line Chart (Year-Month chronological sorting), Donut Chart: Shipment Count by Team

📊 Sheet 4 - Amount per Box Efficiency
Business Question: Who is selling premium value per unit?
Measures:
daxTotal Boxes = SUM(Shipments[Boxes])
Amount per Box = DIVIDE([Total Amount], [Total Boxes])

📊 Sheet 5 - Top & Bottom Performers
Business Question: Who are our best and worst performing salespeople?
Metrics Used: Profit %, Total Profit | Top N / Bottom N Filters applied
Business Impact: Incentive program design, underperformance identification, territory reassignment decisions.

📊 Sheet 6 - Year-over-Year (YoY) Growth Analysis
Business Question: Are we improving compared to last year?
DAX Measures:
daxTotal Amount Last Year =
CALCULATE(
  [Total Amount],
  SAMEPERIODLASTYEAR(Calendar[Date])
)

Total Amount 12M Variance =
[Total Amount] - [Total Amount Last Year]

📊 Sheet 7 - Team-Level Performance Dashboard
Business Question: How are teams performing collectively over time?
Business Impact: Team-level profitability insights, strategic planning support, regional growth alignment.

📊 Sheet 8 – Strategic Performance Overview
This page serves as the Executive Decision Layer of the Chocolate Sales Analytics Platform, designed for senior management, sales directors, regional heads, and strategy teams.
🎯 KPI Cards: Total Amount · Total Boxes · Shipment Count · Total Profit · Profit %
Features: CY vs PY comparison, geographic revenue distribution, shipment distribution analysis, top 6 salespersons spotlight, top 6 products by revenue, dynamic date slicer.

🎯 Technical Skills Demonstrated
✔ Star Schema Modeling
✔ Data Transformation (Power Query)
✔ Relationship Design
✔ DAX Calculations
✔ Time Intelligence Functions (SAMEPERIODLASTYEAR)
✔ Profit & Margin Analytics
✔ Performance Ranking (Top N / Bottom N)
✔ KPI Conditional Formatting
✔ Multi-Page Business Storytelling
✔ Advanced Filtering & Slicers
✔ Data Scalability Thinking

👩‍💼 About Me
Varshini Maskapuri – AI-Focused Business Analyst
📍 DeKalb, Illinois
🎓 MS in Management Information Systems – Northern Illinois University
Certifications:

🏅 Databricks Accredited Generative AI Fundamentals (2026)
🏅 AWS – Generative AI Business Strategy and Solution Design (2026)
🏅 Anthropic – Introduction to Agent Skills (2026)

🔗 LinkedIn
📧 maskapurivarshini@gmail.com

This project is part of my Business Analyst portfolio demonstrating proficiency in Power BI, DAX, data modeling, and business intelligence.
