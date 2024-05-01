---
layout: page
title: Scenario 1 - High volume, batched, file-based GL transactions
description: 01 D365 F&O Integration Best Practices, Patterns and Anti-Patterns
updated: 2024-04-30
permalink: /skilling/d365-academy/business-applications/finops implementation best practices and patterns/intscenario-01
tags:
- business applications
- finance and operations
- integration patterns
- finops implementations
---

# D365 F&O Integration Best Practices, Patterns and Anti-Patterns

## Scenario # 1 - High volume, batched, file-based GL transactions
The customer has a requirement to import GL transactions: High volume, Batched, File-based


## Patterns
GL transactions integration - Inbound

* Data integration through Data management API. 

* Data can be prepared using data integration tools, for example Azure Data Factory (ADF), then sent to F&O via Logic Apps or Azure Function or ADF Web Activity.

## Anti-Patterns
* DO NOT Import through Excel add-in

* DO NOT use OData call per record or OData Batch