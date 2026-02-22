Chocolate Sales Analytics Platform – Power BI

Overview:

Designed and developed a multi-page Power BI analytics solution using star schema modeling, DAX-based time intelligence, and executive KPI architecture. The model was built to simulate an enterprise-ready BI system capable of scaling from Excel to SQL/Azure environments.

Data Architecture:

Fact Table

Shipments (Amount, Boxes, Shipment Date, Product ID, Geo ID, Salesperson ID)

Dimension Tables:

Product
Salesperson
Geography
Calendar (Dedicated Date table)

Modeling Approach:

Star schema design
One-to-many relationships
Surrogate keys
Calendar-based time intelligence
Optimized cross-filtering

Core DAX Implementations:

Total Amount
Total Cost
Total Profit
Profit %
Shipment Count
Amount per Box
SAMEPERIODLASTYEAR
12-Month Variance

Time Intelligence:

Total Amount Last Year =CALCULATE([Total Amount],SAMEPERIODLASTYEAR(Calendar[Date]))

![WhatsApp Image 2026-02-19 at 23 28 50](https://github.com/user-attachments/assets/e2e4defb-9d03-4178-ba79-fc8a04c13581)


Advanced Techniques Used:

Data binning (25-box grouping for histogram clarity)
Conditional formatting using measure logic
Top N / Bottom N dynamic ranking
Multi-page drill-through experience
Executive KPI cards (new Power BI visuals)
Chronological month sorting (Month Number)

Business Outcomes Enabled:

Margin analysis by product & geography
Year-over-year revenue tracking
Salesperson efficiency ranking
Shipment distribution visibility
Team-level performance evaluation
