---
layout: page
title: Core
description: 04 D365 F&O Integration Best Practices, Patterns and Anti-Patterns
updated: 2024-04-30
permalink: /skilling/d365-academy/business-applications/finops implementation best practices and patterns/intscenario-04
tags:
- business applications
- finance and operations
- integration patterns
- finops implementations
---

# D365 F&O Integration Best Practices, Patterns and Anti-Patterns

## Scenario # 1 - Loading large volume of data in batch mode (Import in batch)
Loading large volume of data in batch mode (Import in batch) is taking same amount of time as it takes in asynch import (Import now). It is not possible for the business to complete data loading within the defined cut-over time.

## Patterns
Optimize data migration performance through bundling and iterative performance testing

* Use Import in batch to leverage multi-threading capabilities

* Use Import threshold record count and Import task count to utilize batch bundling

* Determine appropriate value of threads, threshold record count, import task count etc. based on data size & number of available batch threads.

* Data migration performance testing is an iterative process; thus it is suggested that information regarding each test is collected and compared, to determine the optimal configuration for a specific entity


## Anti-Patterns
* DO NOT import large data interactively

* NO plan for data migration performance testing and tuning

* DO NOT use production for data migration testing.

* DO NOT plan single iteration data migration.
