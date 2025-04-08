---
layout: page
title: Scenario 06 - Automation of vendor invoices (inbound and outbound)
description: 06 D365 F&O Integration Best Practices, Patterns and Anti-Patterns
updated: 2025-02-10
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/intscenario-06
tags:
- d365 academy
- business applications
- finance and operations
- integration patterns
- finops implementations
---

# D365 F&O Integration Best Practices, Patterns and Anti-Patterns

## Scenario # 6 - Automation of vendor invoices (inbound and outbound)
Customer wants end-to-end automation of vendor invoices (inbound or outbound)

## Patterns
AP Automation - Inbound or Outbound

* Basic requirements
*   Inbound - Build integration using provided OOB packages as per [vendor invoice automation](https://learn.microsoft.com/en-us/dynamics365/finance/accounts-payable/vendor-invoice-automation)
*   Outbound – Batched export / BYOD
* Power Automate + Azure Form Recognizer API + F&O connector
* Advanced requirements: Evaluate an ISV


## Anti-Patterns
* Using Excel add-in