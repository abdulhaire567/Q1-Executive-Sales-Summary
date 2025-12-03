# Quarter One Sales Analysis – Adventure Works

**Author:** Abdulhaire Rahaman    
**Date:** 2023-11-3  

---

## Case Study / Project Scenario
Jamie, at Adventure Works, is attending a management meeting and has been asked to prepare an Excel file that presents sales figures for Q1 and compares these figures to the same period in the previous year. The management team also wants insight into the sales performance of individual product lines.

**Project Objectives:**
1. Calculate total Q1 sales for 2022 and 2023.  
2. Calculate the percentage increase in sales for 2023.  
3. Break down totals by month.  
4. Create a PivotTable for individual product and product category analysis.

---

## Project Overview
This project demonstrates the use of Excel for executive reporting. It includes data cleaning, formulas, tables, and PivotTables to produce an interactive report for management.  

Key techniques applied:
- Formulas for total sales, monthly breakdowns, tax, and percentage increase.  
- Logical formulas (`IF`) for conditional calculations.  
- Use of Excel Tables for organized datasets.  
- PivotTables with slicers for dynamic analysis.  
- Formatting and presentation improvements.

---

## Data Overview
| Column | Description | Notes |
|--------|------------|-------|
| Product Name | Name of the product | Converted to Proper Case using `PROPER()` |
| Product Category | Category of product | Used in PivotTable Slicer |
| Order Date | Date of sale | Extracted Month and Year |
| Retail Price | Price per unit | Multiplied by quantity for totals |
| Quantity Sold | Units sold | Used in sales calculations |
| Order Total | Calculated as Retail Price × Quantity | Formula applied across dataset |
| Tax | Calculated if Order Total > 2000 | Formula: `=IF(P2>2000,P2*0.05,0)` |

> Dataset used: `Quarter One Report.xlsx` (full dataset included in `data/` folder)

---

## Methodology
1. **Data Cleaning & Formatting**
   - Converted product names to proper case.  
   - Sorted data by Order Date.  
   - Hid irrelevant columns.  
   - Freeze Panes applied to keep headings visible.  

2. **Formulas & Calculations**
   - Total sales for 2022 and 2023 using `SUMIFS`.  
   - Monthly totals using `SUMIFS` by month criteria.  
   - Percentage difference: `(2023_Total - 2022_Total)/2022_Total`.  
   - Tax calculated using `IF` function.  
   - Order Total calculated as `Retail_Price × Quantity`.  

3. **Tables & PivotTables**
   - Converted data range into a Table named `Sales_details`.  
   - Created PivotTable on a new worksheet (`Product Analysis`).  
   - PivotTable fields:  
     - Rows: Product Name  
     - Values: Order Total (sum and % of grand total)  
   - Added Slicers: Product Category & Year  
   - Applied Tabular Form layout and custom number formatting.

---

## Key Findings
| Metric | Result |
|--------|-------|
| Total Sales 2022 | $330,000 |
| Total Sales 2023 | $453,830 |
| Percentage Increase | 37.32% |
| Top Performing Product | Product Name |
| PivotTable Analysis | Interactive dashboard available |

> PivotTable provides management with quick insight into sales per product and category.

---

## Formulas Used
| Formula | Purpose |
|---------|---------|
| `=SUMIFS(R2:R246,L2:L246,2022)` | Total sales for 2022 |
| `=SUMIFS(R2:R246,L2:L246,2023)` | Total sales for 2023 |
| `=(C6-B6)/B6` | Percentage increase |
| `=MONTH(J2)` / `=YEAR(J2)` | Extract month and year from order date |
| `=P2*0.05` | Tax calculation if order total > 2000 |
| `=IF(P2>2000,P2*0.05,0)` | Conditional tax logic |

---

## Challenges & Solutions
- Blended product names → Used `PROPER()` to standardize formatting.  
- Empty cells in monthly totals → SUMIFS ignores blanks.  
- PivotTable formatting → Applied Tabular Form and custom number formatting.  

---

## Next Steps
- Automate quarterly reporting using **Power Query**.  
- Add charts and conditional formatting for visual insights.  
- Expand analysis to full-year dashboards.  

---

## Screenshots
Include screenshots of the following:
1. **Sample Dirty Datasets before cleaning**
2. **Sample Summary Table with totals and percentages**  
3. **PivotTable for Product Analysis and Slicers showing interactive filtering**   

**Sample Dirty Dataset**
![Dirty_Data](https://github.com/abdulhaire567/Q1-Executive-Sales-Summary/blob/092422b4aa16b0a1191d0a876c24b105c35b3b0e/dirtydatasett.png)

**Sample Cleaned Data into table**
![Cleaned Data into table](https://github.com/abdulhaire567/Q1-Executive-Sales-Summary/blob/9e69a2e1db6ab0750baf74f57705ce399a321d39/tablee.png)

**PivotTable for Product Analysis and Slicers showing interactive filtering**
![Pivot Table](https://github.com/abdulhaire567/Q1-Executive-Sales-Summary/blob/24191c11b8e216be058602da215dc9f3747a0a00/pivot%20table.png)

