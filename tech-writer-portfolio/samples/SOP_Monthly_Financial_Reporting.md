# SOP: Monthly Financial Reporting

## Purpose
Define the standardized steps to prepare, validate, and publish monthly financial reports and variance analysis.

## Scope
Finance, Compliance, and Operations teams using Excel and Power BI.

## Prerequisites
- Access to the financial data source
- Excel template v2.1 and Power BI workspace permissions

## Procedure
1. Extract monthly actuals from the data source and save as `Actuals_YYYYMM.xlsx`.
2. Refresh the Excel template using the Data ribbon → Refresh All.
3. Validate the following checks:
   - Total expense equals sum of departmental expenses
   - Month and fiscal period alignment
   - No blank cost center codes
4. Export charts and tables to Power BI and publish to the `Finance-Reporting` workspace.
5. Complete the variance explanation section (timing vs. overspend).
6. Submit report link and change log in Confluence.

## QA Checklist
- [ ] Excel formulas intact (no `#REF!`)
- [ ] Pivot filters reset
- [ ] KPI definitions included
- [ ] Data freshness timestamp present

## Versioning
- Owner: Finance Ops
- Last Updated: 2025-10-15
