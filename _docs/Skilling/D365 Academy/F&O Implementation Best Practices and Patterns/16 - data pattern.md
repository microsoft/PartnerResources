---
layout: page
title: Scenario 06 - customer needs to have as much historical sales data as possible
description: 05 D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns
updated: 2024-04-30
permalink: /skilling/d365-academy/business-applications/finops implementation best practices and patterns/dmscenario-06
tags:
- d365 academy
- business applications
- finance and operations
- data patterns
- finops implementations
---

# D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns

## Scenario # 6 - customer needs to have as much historical sales data as possible
To help guarantee the accuracy of demand forecasts, the customer needs to have as much historical sales data as possible.


## Patterns
Aggregate and use Historical External Demand entity

* Utilize the Historical external demand data entity to import historical data for demand forecasts.

* Aggregate the historical demand transactions (Site, Date, Quantity, Item, Item allocation key)


## Anti-Patterns
* DO NOT import sales order history

* DO NOT import granular demand transactions 