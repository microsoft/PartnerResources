---
layout: page
title: Scenario 05 - High volume/availability e-Commerce pricing
description: 05 D365 F&O Integration Best Practices, Patterns and Anti-Patterns
updated: 2024-04-30
permalink: /skilling/d365-academy/business-applications/finops implementation best practices and patterns/intscenario-05
tags:
- d365 academy
- business applications
- finance and operations
- integration patterns
- finops implementations
---

# D365 F&O Integration Best Practices, Patterns and Anti-Patterns

## Scenario # 5 - High volume/availability e-Commerce pricing
High volume/availability e-Commerce pricing
* Third party e-Commerce framework
* Millions of customers
* Hundred thousand products
* Complex pricing / trade agreements


## Patterns
High volume/availability e-Commerce pricing

* Caching of price and discount data in a middle tier outside F&O
    * Variant 1: Middleware -> Example: Dynamics 365 for Commerce RCSU
    * Variant 2: Middleware -> Example: 3rd party pricing service

* You must either duplicate the pricing logic or cache all permutations. This may be impractical if very complex.If pricing is too complex or volatile, then consider a near real-time pattern which does not block the UI.

## Anti-Patterns
* Real-time (synchronous) price lookups for all search results

* High degree of coupling between ERP and e-commerce systems.

* Routing of service calls to pricing service through F&O

* Over-loading the ERP with item price OData queries. These could get throttled as well.Under load, blocking price lookups would make the e-commerce site seem slow. 
