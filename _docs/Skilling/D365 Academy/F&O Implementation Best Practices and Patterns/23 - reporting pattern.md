---
layout: page
title: Scenario 03 - For Month-end closing Business needs to extract and merge data from multiple reports
description: 03 D365 F&O Reporting Best Practices, Patterns and Anti-Patterns
updated: 2024-09-09
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/repscenario-03
tags:
- d365 academy
- business applications
- finance and operations
- reporting patterns
- finops implementations
---

# D365 F&O Reporting Best Practices, Patterns and Anti-Patterns

## Scenario # 3 - For Month-end closing Business needs to extract and merge data from multiple reports
For month end process, customer needs to generate a list of reports. Business users extract data from all these reports into spreadsheet and then prepare the final report to identify accrual entries they have booked, as part of the month-end close.  

## Patterns
* Utilize Power BI to simplify the operations by combining multiple data points to produce the outcome.

* Instead of creating multiple SSRS reports and list pages to extract data, build a Power BI dashboard to combine required data points to produce desired output which business users are expecting in the excel report.This approach can simplify operations and make month end process more efficient.   

## Anti-Patterns
* DO NOT create a custom SSRS report
* DO NOT use SSRS report to just export data to Excel

