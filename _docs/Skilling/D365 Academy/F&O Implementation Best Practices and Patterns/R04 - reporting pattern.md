---
layout: page
title: Scenario 04 - Financial Statements and Reports
description: 04 D365 F&O Reporting Best Practices, Patterns and Anti-Patterns
updated: 2025-02-10
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/repscenario-04
tags:
- d365 academy
- business applications
- finance and operations
- reporting patterns
- finops implementations
---

# D365 F&O Reporting Best Practices, Patterns and Anti-Patterns

## Scenario # 4 - Financial Statements and Reports
Customer needs to generate financial statements including balance sheet, income statement, profit and loss account, cash flow statement, and so on at any point in time or at the end of defined financial periods. 

## Patterns
Use Financial reporting feature to generate financial reporting 

Financial reporting, previously known as Management reporter, is embedded within Finance and Operations. This tool can be used to design and generate financial reports. To jumpstart financial reporting, Microsoft provides multiple default financial reports, which can be modified to suit the business needs of any customer.


## Anti-Patterns
* DO NOT build SSRS reports for Financial reporting 
* DO NOT export data outside to generate financial report except for data mash-up scenarios.

