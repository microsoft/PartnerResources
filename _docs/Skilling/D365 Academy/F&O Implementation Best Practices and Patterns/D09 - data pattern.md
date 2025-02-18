---
layout: page
title: Scenario 09 - Data Migrations from legacy systems involving multiple legal entitites
description: 09 D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns
updated: 2025-02-10
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/dmscenario-09
tags:
- business applications
- finance and operations
- data patterns
- finops implementations
---

# D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns

## Scenario # 9 - Data Migrations from legacy systems involving multiple legal entitites
The business has large number of legal entities in Dynamics 365. Customer has created multiple folders for each legal entity (on prem). The customer is extracting data from legacy application and generating one file for one data entity for each legal entity and placing the data file into respective legal entity folder. 


## Patterns
Utilize Recurring Integration Scheduler (RIS) for automating data movement 

* Set up input folders for each legal entity
* Leverage either data projects OR package template option within RIS, to create data packages (zip file) with data and meta data.
* Set up recurring job in RIS and manage RIS configuration (import/export)


## Anti-Patterns
* DO NOT develop X++ code to manage the files.