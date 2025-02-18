---
layout: page
title: Scenario 01 - Loading large volume of data using Data Management Framework
description: 01 D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns
updated: 2025-02-10
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/dmscenario-01
tags:
- d365 academy
- business applications
- finance and operations
- data patterns
- finops implementations
---

# D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns

## Scenario # 1 - Loading large volume of data using Data Management Framework
Loading large volume of data using Data Management Framework is taking longer than the defined cut-over time. Data can only be migrated during defined cutover window.

## Patterns
Optimize data migration performance with the use of right data entity and configuration

* Evaluate the appropriate custom or standard data entity- Use entities that support muti-threading like Customer definitions(CustCustomerBase) and Customer detail (CustCustomerDetailsV2)

* Disable change tracking for data migration

* Use bulk import by enabling set-based processing (note - not all entities support set-based processing)


## Anti-Patterns
* DO NOT enable change tracking

* DO NOT use composite data entity

* DO NOT turn-on X++ business validations

* DO NOT use SQL to migrate data