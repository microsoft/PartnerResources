---
layout: page
title: Data Migration scenario 04 - The business has high volume of data
description: 04 D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns
updated: 2024-04-30
permalink: /skilling/d365-academy/business-applications/finops implementation best practices and patterns/dmscenario-04
tags:
- d365 academy
- business applications
- finance and operations
- data patterns
- finops implementations
---

# D365 F&O Data Migration Best Practices, Patterns and Anti-Patterns

## Scenario # 4 - The business has high volume of data
The business has high volume of data that needs to be migrated to Dynamics 365. Significant portion of the data is non-volatile master data. Conversion of the whole dataset will not be feasible during the cutover downtime window. 

The customer will be running mock cutover testing during the days leading up to Go-Live.



## Patterns
Execute pre-conversion in Sandbox Environments

* The customer must have successfully completed UAT, have a stable code base and configuration and be able to designate a Tier 2/2+ sandbox as a staging environment.  This environment can be loaded with the final configuration data and then data migration of non-volatile entities can begin ahead of the cutover downtime window in the sandbox environment.


* Production environment can be refreshed from this sandbox, post which, mock cutover testing can be conducted. Execute point-in-time restore, if applicable. Once the cutover is ready to commence, the only task left will be to migrate opening balances and the delta master data.


## Anti-Patterns
* DO NOT do pre-conversion in Cloud Hosted Environments

* DO NOT attempt to pre-migrate volatile data sets

* DO NOT attempt pre-migration with unstable configurations

