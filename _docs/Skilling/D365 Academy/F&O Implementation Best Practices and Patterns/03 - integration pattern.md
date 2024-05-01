---
layout: page
title: Scenario 03 - propagate information about order confirmations to multiple outbound systems
description: 03 D365 F&O Integration Best Practices, Patterns and Anti-Patterns
updated: 2024-04-30
permalink: /skilling/d365-academy/business-applications/finops-implementation-bestpractices-and-patterns/intscenario-03
tags:
- d365 academy
- business applications
- finance and operations
- integration patterns
- finops implementations
---

# D365 F&O Integration Best Practices, Patterns and Anti-Patterns

## Scenario # 3 - propagate information about order confirmations to multiple outbound systems
Customer has the need to propagate information about order confirmations to multiple systems:
* Immediately notify a department head (via email) 
* Add confirmed order to a SharePoint list.
* Record the Id of the confirmed order in an external system (SQL DB).


## Patterns
Publish-subscribe messaging

* Standard or custom Business Event, to a Service Bus Topic, 3 subscriptions

* Use Logic App/Power Automate flows and built-in connectors
    * For sending e-mail notification
    * Inserting into SharePoint list
    * Inserting record into SQL server

* Create your own Business Event when the integration requirements are right (small and nimble messages, no bulk data, business process driven context). Custom business events are quite straightforward.

* Consider out of the box tools in Azure to minimize point-to-point integrations and support pub-sub or multiplexing/demultiplexing. Standard connectors are much easier than writing your own client for an API.

* For pub-sub, consider the consumer with the shortest required latency (e.g. notifications could be needed closer to real-time than the other end-points)


## Anti-Patterns
* DO NOT Use custom code to call all three consumers directly.

* Build different triggers for the three consumers.

* Ignore latency requirements in the scenarios (for example, timely notifications).

