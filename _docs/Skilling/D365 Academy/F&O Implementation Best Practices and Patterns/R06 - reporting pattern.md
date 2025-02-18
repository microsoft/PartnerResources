---
layout: page
title: Scenario 06 - Reports that require data mash-up between various on-prem and cloud apps 
description: 06 D365 F&O Reporting Best Practices, Patterns and Anti-Patterns
updated: 2025-02-10
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/repscenario-06
tags:
- d365 academy
- business applications
- finance and operations
- reporting patterns
- finops implementations
---

# D365 F&O Reporting Best Practices, Patterns and Anti-Patterns

## Scenario # 6 - Reports that require data mash-up between various on-prem and cloud apps
Customer needs dashboards and analytical reports that require data mash-up between Finance and Operations, Human Resources, Customer Engagement apps and other on-prem and cloud apps 


## Patterns
Bring Finance and Operation and CDS data to Azure Data Lake. Use Synapse Analytics to ingest, curate and build analytics. 
* Use Data feeds feature to bring Finance and Operations apps data to customers own Azure Data Lake. 
* Bring CDS data to Azure Data Lake using Export to data lake feature. 
* Use Synapse Analytics to ingest data from other systems, curate and stage final data and build Power BI report to serve.



## Anti-Patterns
* DO NOT use Dual-write to copy Finance and Operations data to CDS
* DO NOT bring Finance and Operations and CDS data on-premise to build dashboards