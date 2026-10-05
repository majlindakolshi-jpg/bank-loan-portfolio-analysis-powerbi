# Bank Loan Portfolio & Risk Analysis Dashboard

## Overview
An interactive Power BI dashboard designed to analyze bank loan distribution, portfolio risk exposure, and overdue metrics across various branches. The dataset was processed and modeled directly from Excel source files into Power BI Desktop.

## Key Features & Analytics
- **Portfolio Performance:** Tracked total loan distribution, active loans, and branch-level metrics.
- **Risk & Overdue Monitoring:** Evaluated portfolio risk (PAR) and overdue percentages to identify high-risk loan categories and branches.
- **Data Modeling & Analytics:** Constructed a Star Schema data model with custom DAX measures for key financial indicators.

## Tools & Technologies Used
- **Power BI Desktop:** Data transformation (Power Query), Data Modeling (Star Schema), DAX calculations, and Report Visualization.
- **Microsoft Excel:** Source dataset.

## Key DAX Measures
- `Total Loans` = SUM(Loans[LoanAmount])
- `Overdue Amount` = CALCULATE(SUM(Loans[LoanAmount]), Loans[Status] = "Overdue")
- `Overdue %` = DIVIDE([Overdue Amount], [Total Loans], 0)
