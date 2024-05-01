---
layout: page
title: Scenario 04 - credit check / limit assignment is done with external service call
description: 04 D365 F&O Integration Best Practices, Patterns and Anti-Patterns
updated: 2024-04-30
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/intscenario-04
tags:
- d365 academy
- business applications
- finance and operations
- integration patterns
- finops implementations
---

# D365 F&O Integration Best Practices, Patterns and Anti-Patterns

## Scenario # 4 - credit check / limit assignment is done with external service call
Customer credit check / limit assignment is done with external service call. Credit process is run for new customer during order capture.Credit process can take 1-2 minutes to complete.This process is used in a high-volume call center


## Patterns
Interactive asynchronous service invocation

* Create order with active hold. Create batch task with pop-up alert, to call external service and then clear hold upon successful credit processing.

In the pattern recommended, the end user experience (e.g. response time) does not take a dependency on the latency of the external service call, while still allowing the process to quickly alert the user via the message center.



## Anti-Patterns
* Synchronous, blocking call to external service while the end user session waits on the results.
