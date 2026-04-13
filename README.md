Finance Intelligence Hub: End-to-End Sales & Profitability Analysis

Project Overview

The Finance Intelligence Hub is a comprehensive data analytics project designed to transform raw financial records into a strategic decision-support tool. This project demonstrates the full analytical lifecycle—from data extraction and cleaning to advanced DAX modeling and interactive executive storytelling.

The goal was to move beyond static reporting to provide Scenario Modeling (What-If analysis) that identify the core drivers of global profitability.

Technical Stack

• Data Sourcing: Microsoft Financial Sample Dataset.

• ETL & Data Cleaning: Power Query (M).

• Data Modeling: Star Schema Methodology.

• Calculations: Advanced DAX (Data Analysis Expressions).

• Visualization: Power BI Desktop.

The Process: Step-by-Step

1. Data Acquisition & ETL (Power Query)

The raw data was imported and subjected to a rigorous cleaning process in Power Query to ensure a "Single Source of Truth."

• Standardization: Fixed data types for currency, dates, and geographic regions.

• Attribute Cleaning: Removed null values and handled inconsistencies in the Product and Segment columns.

• Date Normalization: Ensured the date grain was consistent across all transactions.

2. Data Modeling (The Star Schema)

To optimize performance and enable Time Intelligence, I moved away from a flat-file structure.

• Calendar Table: Created a custom DAX Calendar table to avoid gaps in time-series analysis.

• Relationships: Established a 1:Many relationship between the Calendar table and the Financials fact table.

• Measures Table: Created a dedicated table to house all 15+ DAX measures for better organization.

3. Advanced DAX Engineering

I developed a library of measures focused on business momentum and efficiency:

• Core Metrics: Total Sales, Total Profit, Total Cost, and Total Orders.

• Time Intelligence:

• YoY Growth %: \text{DIVIDE}([Total\ Sales] - [Sales\ PY], [Sales\ PY], 0)

• MoM Growth %: Calculating momentum shifts month-over-month.

• Profitability Metrics: Profit Margin % and Average Order Value (AOV).

• What-If Logic: Created a dynamic Projected Profit measure that responds to a user-controlled cost reduction parameter.

4. Interactive Visualization

The dashboard was designed using the F-Pattern layout for maximum executive readability.

• KPI Header: High-impact cards with Reference Labels showing growth indicators.

• Trend Analysis: An Area Chart comparing revenue over months

• Breakdown: A Decomposition Tree that allows users to drill down from Profit into specific Segments and Countries.

• Audit Table: A Matrix visual with conditional formatting (Data Bars and Icons) for a detailed regional audit.

Key Business Insights

• Exponential Growth: Identified a 349% YoY Revenue increase in specific periods, primarily driven by the Government segment.

• Efficiency Drivers: The dashboard revealed that while sales volume was high in some regions, the Profit Margin was significantly higher in others, suggesting a need for localized pricing strategies.

• Simulation Power: The What-If parameter demonstrates that a 5% reduction in production costs could lead to a $1.2M+ increase in net profit.

How to Use

1. Clone the Repo: Download the .pbix file.

2. Open in Power BI Desktop: Explore the data model and DAX formulas.

3. Interact: Use the slicers for Year, Country, and the Cost Reduction slider to see real-time shifts in the data.

👤 Author

Okoli Ifechukwu Chinwe

• LinkedIn: http://linkedin.com/in/ife-okoli

• Background: Pharmacist transitioned into Data Analytics, focused on building data-driven solutions for complex business problems.

