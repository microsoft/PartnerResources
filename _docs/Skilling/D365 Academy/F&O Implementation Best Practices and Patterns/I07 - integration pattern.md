---
layout: page
title: Scenario 07 - Complex batch scheduling
description: 07 D365 F&O Integration Best Practices, Patterns and Anti-Patterns
updated: 2025-02-10
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/intscenario-07
tags:
- d365 academy
- business applications
- finance and operations
- integration patterns
- finops implementations
---

# D365 F&O Integration Best Practices, Patterns and Anti-Patterns

## Scenario # 7 - Complex batch scheduling
* Customer has enterprise processes that span multiple systems. 
* Job are initiated in legacy systems that must complete before Dynamics 365 executes subsequent batch jobs
* Multiple batch jobs in Dynamics need to run, but may not overlap


## Patterns
* Centralized batch control system calls custom service to create a non-recurring batch task, listen for batch completion business event / poll for finished status
* Use Job Dependencies in F&O and define that Job X is dependent on Job Y
* As F&O only handles batch task dependencies within a single batch job, it would be much simpler if scheduling is based on sufficient time gaps


## Anti-Patterns
* Scheduling batch jobs for exgternal systmes in F&O