---
layout: page
title: Integration scenario 02 - sales orders from 3rd party system(s)e
description: 02 D365 F&O Integration Best Practices, Patterns and Anti-Patterns
updated: 2024-04-30
permalink: /skilling/d365-academy/business-applications/finops implementation best practices and patterns/intscenario-02
tags:
- d365 academy
- business applications
- finance and operations
- integration patterns
- finops implementations
---

# D365 F&O Integration Best Practices, Patterns and Anti-Patterns

## Scenario # 2 - sales orders from 3rd party system(s)
Customer needs to create sales orders that are coming from 3rd party system(s) (for example, Salesforce, B2B web shop, Amazon, …)
* Up to 20k Sales Lines per hour in high season from B2B web shops
* 500 Sales Lines per hour peak from Salesforce


## Patterns
Sales order entry - Inbound

* Low volume: OData
    * Benefit: Simpler error handling and multi-system transactionality.

* High volume: Batched integration through 
    * Data Management API
    * Or Custom Services

## Anti-Patterns
* Complex entity through OData batch for high volume inbound

* Expensive subsequent logic on entity (ex: intercompany, Available to Promise (ATP) / Capable to Promise (CTP) checks, etc.)


