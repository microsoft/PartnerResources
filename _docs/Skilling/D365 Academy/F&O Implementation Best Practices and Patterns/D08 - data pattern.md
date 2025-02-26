---
layout: page
title: Scenario 08 - Importing large volume of GL Journals
description: 08 D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns
updated: 2025-02-10
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/dmscenario-08
tags:
- business applications
- finance and operations
- data patterns
- finops implementations
---

# D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns

## Scenario # 8 - Importing large volume of GL Journals
The customer is importing substantially large volume of journal balances. Journal name is defined as ‘In connection with balance’ where each time a voucher is balanced, a new voucher number is assigned. 


## Patterns
Optimize Number Sequence approach

* Avoid the logic of fetching a number sequence value by including the value directly in the data file

* Update the “next number” in number sequence after importing the data

* If number sequence is absolutely needed to be used: Use pre-allocated number sequence



## Anti-Patterns
* DO NOT use continuous number sequence unless it’s a legal requirement.