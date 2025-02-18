---
layout: page
title: Scenario 03 - Data loading slows down after importing large volume of data 
description: 03 D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns
updated: 2025-02-10
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/dmscenario-03
tags:
- d365 academy
- business applications
- finance and operations
- data patterns
- finops implementations
---

# D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns

## Scenario # 3 - Data loading slows down after importing large volume of data 
Data loading slows down after importing large volume of data in the initial set of legal entities. Performance keeps deteriorating for the same data entity for subsequent data loads in other legal entities. 


## Patterns
Warm up and statistics management

* Clean up history using staging clean up

* Prior to running a data migration job for a large volume of data consider updating the statistics across the associated tables/entire database.


## Anti-Patterns
* Lack of review of performance telemetry – e.g., indexes, query plan etc.

* DO NOT use Tier-1 environment for Data Migration.

