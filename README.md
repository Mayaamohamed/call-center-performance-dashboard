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

**2. Data Modeling & Advanced Calculations (Power Pivot & DAX)**
* Built dynamic DAX Measures for weighted KPIs to avoid "average of averages" calculation errors.
* Developed custom formulas for key operational metrics:
  * **Answer Rate & Abandoned Rate:** Evaluated overall volume handling.
  * **Service Level %:** Measured percentage of calls answered within 20 seconds.
  * **Average Handle Time (AHT) & ASA:** Calculated average durations using sum-based logic.
  * **Satisfaction Score (CSAT):** Weighted ratings based on unique survey responses.
  * **Overall Weighted KPI Score:** Combined weighted metrics (35% CSAT, 30% AHT, 20% Answered, 15% ASA) into a single performance index.

**3. Interactive Visual Design & UI/UX**
* Built custom KPI cards using grouped dynamic text boxes linked directly to Pivot measures.
* Integrated custom formatting (`mm"m":ss"s"`, `00"s"`) to present time-based variables accurately.
* Designed clean, focused visualizations including Top 5 Team Leader breakdowns for AHT, ASA, and CSAT.

**4. Business Storytelling & Executive Summary**
* Translated dashboard metrics into an executive summary highlighting operational gaps (e.g., Service Level underperformance at 60%).
* Formulated data-driven recommendations for shift rescheduling and targeted agent coaching.
