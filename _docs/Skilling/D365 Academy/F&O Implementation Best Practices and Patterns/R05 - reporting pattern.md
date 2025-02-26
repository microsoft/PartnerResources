---
layout: page
title: Scenario 05 - For Month-end closing Business needs to extract and merge data from multiple reports
description: 05 D365 F&O Reporting Best Practices, Patterns and Anti-Patterns
updated: 2025-02-10
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/repscenario-05
tags:
- d365 academy
- business applications
- finance and operations
- reporting patterns
- finops implementations
---

# D365 F&O Reporting Best Practices, Patterns and Anti-Patterns

## Scenario # 5 - For Month-end closing Business needs to extract and merge data from multiple reports
Customer needs to generate regulatory, tax reporting and payment documents to serve the local government or banking institutions. These reports have a pre-defined layout and format defined by the public agencies and must be delivered in paper or electronic format.

Examples: Intrastat trade document for Europe, Sales list for Europe, Tax reporting BAS  for Australia,  ISO20022 Credit transfer, BACS Vendor payment file for UK, JBA Payment file for Japan etc.


## Patterns
Use Electronic reporting to configure country specific regulatory, tax reporting and payment documents
* ER reporting solves many country-specific incoming and outgoing electronic documents needs. 
* Download and evaluate updates ER templates provided in LCS.


## Anti-Patterns
* DO NOT build SSRS reports for regulatory reporting 
* DO NOT create custom batch jobs to generate files
* DO NOT export data to generate regulatory reports