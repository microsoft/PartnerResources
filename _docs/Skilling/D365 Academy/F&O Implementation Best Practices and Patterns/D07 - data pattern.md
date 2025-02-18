---
layout: page
title: Scenario 07 - Master data lying in multiple disparate systems partly due to M&A
description: 07 D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns
updated: 2025-02-10
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/dmscenario-07
tags:
- business applications
- finance and operations
- data patterns
- finops implementations
---

# D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns

## Scenario # 7 - Master data lying in multiple disparate systems partly due to M&A
As-is, business uses different systems across its multiple geographical locations and has been maintaining their customers in a disparate manner across the locales – partly due to the mergers and acquisitions they have been undergoing in the recent years. But having customer information in different systems was making it impossible to get an overall picture of the business. To gain better insight and control of the information, business has decided to create a global customer base. 


## Patterns
Perform data transformation before loading data into Dynamics 365

* Clean up data in legacy systems (source) as much as possible

* Perform ‘data transformation’ outside of Dynamics 365

* Automate ‘data transformation’ as you will need to execute data migration multiple times and to avoid any manual mistakes

* Rectify the errors related to data quality to reduce the code churn for X++ validations and error processing for optimal performance


## Anti-Patterns
* X++ Translation / Conversion during Data Import

* Executing X++ validations during Data Import

* Starting mapping from legacy data structures