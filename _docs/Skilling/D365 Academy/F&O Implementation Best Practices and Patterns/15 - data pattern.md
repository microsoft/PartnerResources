---
layout: page
title: Scenario 05 - Customer plans to use ‘Dual Write (DW)’ infrastructure to integrate data
description: 05 D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns
updated: 2024-04-30
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/dmscenario-05
tags:
- d365 academy
- business applications
- finance and operations
- data patterns
- finops implementations
---

# D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns

## Scenario # 5 - Customer plans to use ‘Dual Write (DW)’ infrastructure to integrate data
The customer is using Dynamics 365 Sales, Human Resources (Dataverse) and Finance and Operations apps. Customer plans to use ‘Dual Write (DW)’ infrastructure to integrate data from Dataverse to Finance and Operations apps and vice-versa. The customer will need to migrate for example, ‘Accounts’ data into Dataverse. Same ‘Accounts’ data will need to move as ‘Customers’ data into Finance and Operations apps at Go-Live.


## Patterns
Keep ‘Data Migration’ separate from Dual Write.


* DW infrastructure is designed to integrate data in near real-time between Dataverse and F&O.

* Use Initial Write/Initial Sync to sync only low volume setup and reference data.

* Initial Write/Initial Sync is not replacement of large volume master or transactions data migration.

* DW infrastructure uses F&O ‘OData’ entities, and it is not suitable for data migration scenarios where bulk data import is needed.

* Migrate master or transactional data separately in Dataverse and F&O before  enabling DW.



## Anti-Patterns
* DO NOT use OData for data migration

* DO NOT use Dataverse/DW as a data migration platform 

* DO NOT practice bad dual mastering approaches 
