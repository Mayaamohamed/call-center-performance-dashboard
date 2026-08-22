# Call Center Performance & Operations KPI Dashboard

📌 **Project Overview**
Designed and developed an end-to-end executive Call Center KPI Dashboard using Microsoft Excel and Power Pivot. The goal was to track operational efficiency, agent responsiveness, and customer satisfaction metrics against corporate goals to deliver actionable recommendations for management.

---

🛠️ **Tech Stack & Key Features**
* **Data Processing & ETL:** Power Query
* **Data Modeling & Analytics:** Power Pivot, DAX (Data Analysis Expressions)
* **Visualization & UI Design:** Custom Excel Charts, Dynamic Slicers, Timeline, Conditional Formatting
* **Reporting:** Executive Insights & Strategic Recommendations

---

🚀 **Key Implementation Steps**

**1. Data Extraction & Transformation (Power Query)**
* Cleaned and structured raw call log datasets using Power Query.
* Handled missing values, standardized datetime formats, and performed schema transformations for analysis.

**2. Data Modeling & Data Warehouse Architecture (Power Pivot & DAX)**
* **Snowflake Data Model:** Designed an optimized data model in Power Pivot establishing 1-to-many (`1:*`) relationships between dimension tables and fact tables:
  * **`Call_Log` (Fact Table):** Contains transactional call metrics (Incoming/Answered Calls, Talk/Hold/Handle Durations, Answer Speed, Waiting Time, Service Level). Linked to `Calendar` via `Date` (`* : 1`) and to `Roster` via `AgentID` (`* : 1`).
  * **`CSAT` (Fact Table):** Stores customer satisfaction survey responses (Rating, Rating Status, Category, Sub-category). Linked to `Calendar` via `Date` (`* : 1`) and to `Roster` via `AgentID` (`* : 1`).
  * **`Roster` (Dimension Table):** Serves as the central agent reference, mapping `Agent_Id` and `Agent_name` to organizational structures including `Team Leader [TL]`, `Manager`, `Tenure Bucket`, and `Agent Shift`.
  * **`Calendar` (Dimension Table):** Provides date intelligence hierarchy with fields for `Date`, `Week`, `Month-Year`, `Quarter`, and `Year`.
* **Dynamic DAX Measures:** Built custom measures for weighted KPIs to prevent "average of averages" calculation errors:
  * **Answer Rate & Abandoned Rate:** Evaluated overall volume handling.
  * **Service Level %:** Measured percentage of calls answered within 20 seconds.
  * **Average Handle Time (AHT) & ASA:** Calculated average durations using sum-based duration logic.
  * **Satisfaction Score (CSAT):** Calculated weighted ratings based on unique survey responses.
  * **Overall Weighted KPI Score:** Combined weighted metrics (35% CSAT, 30% AHT, 20% Answered, 15% ASA) into a single unified performance index.

**3. Interactive Visual Design & UI/UX**
* Built custom KPI cards using grouped dynamic text boxes linked directly to Pivot measures.
* Integrated custom formatting (`mm"m":ss"s"`, `00"s"`) to present time-based variables accurately.
* Designed clean, focused visualizations including Top 5 Team Leader breakdowns for AHT, ASA, and CSAT.

**4. Business Storytelling & Executive Summary**
* Translated dashboard metrics into an executive summary highlighting operational gaps (e.g., Service Level underperformance at 60%).
* Formulated data-driven recommendations for shift rescheduling and targeted agent coaching.
