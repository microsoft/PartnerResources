---
layout: page
title: Scenario 02 - Multiple users need different filters and columns for same report to analyze
description: 02 D365 F&O Reporting Best Practices, Patterns and Anti-Patterns
updated: 2024-09-09
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/repscenario-02
tags:
- d365 academy
- business applications
- finance and operations
- reporting patterns
- finops implementations
---

# D365 F&O Reporting Best Practices, Patterns and Anti-Patterns

## Scenario # 2 - Multiple users need different filters and columns for same report to analyze
Multiple users need to analyze the open purchase orders. Each user needs different filters and columns in their reports to analyze and act.

## Patterns
* An operational workspace is designed to be the primary navigation mechanism to support a specific business activity. The list page can be added to operational workspace via personalization as tile, list or link.

* A list page has lower development costs than a SSRS report and is more user friendly than a data entity. Using personalization and Saved view feature you can create scenario specific pages and publish to users or roles. The contents of the list page grid can easily be exported to Excel for further analysis. 


## Anti-Patterns
* DO NOT create a custom SSRS report
* DO NOT use SSRS report to just export data to Excel

