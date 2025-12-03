# Executive-Data-Summary-Sales-Analysis-Q1-2023-Excel-
Executive Data Summary of Q1 2023 sales. Calculates totals, percentage changes, and projects Q2 targets using Excel formulas and PivotTables.
# Executive Data Summary – Sales Analysis Q1 2023

**Author:** Your Name  
**Course:** Coursera – Excel Skills for Business  
**Date:** YYYY-MM-DD  

---

## Case Study / Project Scenario
The dataset represents Q1 2023 sales for multiple teams and team members. The objectives of this project were to:  
1. Calculate the overall sales total.  
2. Break down sales by team and by individual team member.  
3. Compare Q1 2023 sales to Q1 2022 and calculate the percentage difference.  
4. Project Q2 2023 sales targets using a 10% increase.  

All analysis, formulas, and PivotTables in this repository are based on this scenario.

---

## Project Overview
This project demonstrates how Excel can be used for executive reporting and decision-making. Using formulas, PivotTables, and formatting, the analysis provides a clear view of sales performance and future targets.

---

## Data Overview
| Column Name | Description | Notes / Cleaning Required |
|------------|-------------|--------------------------|
| Total Sales | Dollar value of sales per entry | Checked format as Currency |
| Team | Sales team name | Standardized names |
| Team Members | Individual responsible | Corrected blended entries |
| Product | Product category | Extracted using `MID` and `RIGHT` functions |
| Date | Date of sale | Standardized MM/DD/YYYY |
| Other Columns | __________________ | __________________ |

> **Dataset Source:** Simulated dataset from Coursera

---

## Methodology
- **Freeze Panes** for row 1 and column A  
- **Merge & Center** for table headings  
- Applied formulas:  
  - `SUM`, `AVERAGE`, `SUMIF`  
  - `NETWORKDAYS` to calculate weekdays  
  - Percentage difference: `(F10-E10)/E10`  
- Created PivotTables:  
  - Rows: Team → Team Members  
  - Values: Total Sales  
  - Calculated Field: Q2 Target = Total Sales × 110%  
- Applied number formatting: Currency, Percentage, General  

---

## Key Findings
| Metric | Result |
|--------|-------|
| Total Sales Q1 2023 | $XXX,XXX |
| Top Performing Team | Team A |
| Average Sales per Member | $XX,XXX |
| Q2 Target | $XXX,XXX |

> Screenshots are stored in the `screenshots/` folder.  

---

## Formulas Used
| Function / Formula | Purpose | Example |
|------------------|---------|---------|
| `=SUM(E4:E246)` | Total sales | Total Q1 sales |
| `=AVERAGE(C1:C5)` | Average per member | Average sales per team member |
| `=SUMIF(range, criteria, sum_range)` | Conditional sum | Sales > $5,000 |
| `=NETWORKDAYS(A2,B2)` | Count weekdays | Workdays between start and end date |
| `=IF(AND(...),...,...)` | Conditional logic | Discounts or bonuses |
| `=(F10-E10)/E10` | Percentage difference | YoY sales growth |
| PivotTables | Summarize data | Team and member breakdowns |

---

## Challenges & Solutions
- Blended product entries → Used `MID` and `RIGHT` to separate product category  
- Empty cells affected averages → Excel ignores blanks by default  
- Formatting inconsistencies → Standardized currency and dates  

---

## Next Steps
- Automate future reporting using **Power Query**  
- Add charts and conditional formatting for visual insights  
- Expand to full-year sales dashboards  

---

## Screenshots
![Pivot Table](screenshots/pivot_table.png)  
![Q2 Target Calculation](screenshots/q2_target.png)
