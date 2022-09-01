---
layout: page
title: Partner Readiness Resources for Modernizing Java Apps
description: Resources for Modernizing Java Apps
updated: 2022-08-11
permalink: /azure/appdev/modernize-dot-java-apps
tags:
- azure
- appdev
- technical resources 
- learning plan
---

# Partner Readiness Resources for Modernizing Java Apps

## Envisioning Briefing

### Demos & Walkthroughs

<!-- * [Web App Modernization Demo - Video](https://microsoft.sharepoint.com/:p:/t/AppSpecialist/EciMr9FUoWZMuWuPVwm18XkBNSPMMBGuq9XdXP1o-Dpysg?e=jJh1nX)
* [Web App Modernization Demo – Click Through](https://microsoft.sharepoint.com/:p:/t/AppSpecialist/EciMr9FUoWZMuWuPVwm18XkBNSPMMBGuq9XdXP1o-Dpysg?e=jJh1nX) -->
* [Azure Apps Demo](https://azureappsdemomap.com/map)

### Cost Benefit

<!-- * [Apply Azure Hybrid Benefit (AHUB) to Azure SQL Database PaaS services](https://azure.microsoft.com/en-us/services/sql-database/) -->
* [Enterprise Dev/Test Offer](https://azure.microsoft.com/en-us/offers/ms-azr-0148p/#:~:text=The%20Enterprise%20Dev/Test%20offer%20is,be%20accessed%20by%20any%20users.)

## Architectural Design Session

### Discovery

* [App Service Migration Assistant Tool](https://appmigration.microsoft.com/)
<!-- * [App Service Migration Assistant Documentation](https://github.com/Azure/App-Service-Migration-Assistant/tree/master/MigrationDocs) -->
<!-- * [Azure Database Migration Guide](https://datamigration.microsoft.com/) -->
* [Data Migration Service](https://docs.microsoft.com/en-us/azure/dms/)
<!-- * [Data Migration Assistant](https://docs.microsoft.com/en-us/sql/dma/dma-overview?view=sql-server-2017) -->
<!-- * [SQL Server Migration Assistant](https://docs.microsoft.com/en-us/sql/ssma/sql-server-migration-assistant?view=sql-server-2017) -->

(Include third party tools)

### Assessment

(Which apps are candidates for modernization? We have a tool for this)

### Plan

(What are the steps and the order?)

#### App Migration Planning

<!-- * [Architecture, Migration Process, Components](https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/articles/net-app-modernization) -->
<!-- * [Migrate, modernize .NET applications with Azure](https://techcommunity.microsoft.com/t5/apps-on-azure/migrate-modernize-net-applications-with-azure/ba-p/1696499) -->
* [Migration Checklist for Azure App Service](https://azure.microsoft.com/en-us/blog/migration-checklist-when-moving-to-azure-app-service/)
<!-- * [Apps Migration Considerations](https://docs.microsoft.com/en-us/dotnet/azure/migration/app-service) -->
* [Choosing an Azure compute service for your application](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-decision-tree?_lrsc=e623b82d-6c35-449e-9ff0-8cc81a0819e3)

The following Azure services can host a Java application. Consider which is appropriate for the current solution.

* Azure Spring Apps
* Azure App Service
* Azure Kubernetes Service

##### Azure Spring Apps

Azure Spring Apps is a Platform as a Service (PAAS) offering providing hosting, configuration, and Applicatino Lifecycle Management, specifically designed for hosting Java Spring applications.

Read more about Azure Spring Apps [here](https://azure.microsoft.com/en-us/services/spring-apps/).

##### Azure App Service

Azure App Service is a PAAS offering that hosts web applications, REST APIs, and mobile backends. Code can be deployed from a Java application or a number of other languages and platforms.

Read more about Azure App Service [here](https://docs.microsoft.com/en-us/azure/app-service/).

##### Azure Kubernetes Service

Azure Kubernetes Service is a service that allows you to manage Kubernetes clusters within Azure. It supports any application that can run in a container, including Java applications.

Read more about Azure Kubernetes Service [here](https://docs.microsoft.com/en-us/azure/aks/).

#### Database Migration Planning

<!-- * [SQL Migration](https://docs.microsoft.com/en-us/sql/sql-server/migrate/?view=sql-server-2017) -->
* [Choosing Your Database Migration Path](https://azure.microsoft.com/en-us/resources/choosing-your-database-migration-path-to-azure/)

##### Migrate SQL open source DB to Azure DB

##### Migrate NoSQL open source DB to CosmosDB

### Cloud Modernization

(Automate move from on-prem to Azure. What are considerations?)

#### App Modernization

#### Database Modernization

* [Cloud Journey Tracker](https://docs.microsoft.com/en-us/assessments/?mode=pre-assessment&amp;session=f13774ce-3324-46c7-9803-3b0298c49aed)
* [Solutions Assessment](https://www.microsoft.com/en-us/solutionassessments/solutionassessments.aspx?SilentAuth=1)
<!-- * [Migration Plan](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/migrate/azure-best-practices/contoso-migration-refactor-web-app-sql) -->

### Operationalization

Monitoring
Security
Observability
Metrics

## Deployment

* [Best Practices for Azure App Service](https://docs.microsoft.com/en-us/azure/app-service/app-service-best-practices)
* [Azure App Service Deployment Best Practices](https://docs.microsoft.com/en-us/azure/app-service/deploy-best-practices)
* [Highly Available Multi-Region Web Application on Azure](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/app-service-web-app/multi-region)
<!-- * [Highly Available SQL Database on Azure](https://docs.microsoft.com/en-us/azure/azure-sql/database/high-availability-sla) -->
* [Microsoft Azure Well-Architected Framework](https://docs.microsoft.com/en-us/azure/architecture/framework/)
* [Cloud Adoption Framework](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/)
* [Best Practices for Cloud Applications](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)
* [Design Principles for Azure Applications](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/)
* [Application Performance Management (APM) on Azure](https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview)

### Azure Compete Scenarios

* [AWS to Azure services comparison](https://docs.microsoft.com/en-us/azure/architecture/aws-professional/services)
* [GCP to Azure services comparison](https://docs.microsoft.com/en-us/azure/architecture/gcp-professional/services)

## Assessments (Technical & Solution)

[Partner Readiness Resources for Azure Spring Apps](./Partner%20Readiness%20Resources%20for%20Spring%20Apps.md)

## Architecture Design Session

A key part of any application modernization project is to conduct an Architecture Design Session (ADS) with the customer or partner. This is ideally done in-person to avoid distractions; however, it can also be accomplished successfully remotely or as a hybrid event with some attendees meeting in person and others participating virtually.

The goals of an Architectural Design Session are:

* Align the specific capabilities of the Azure platform with the requirements of the customer's project
* Identify areas of risk and prioritize design and development tasks

The steps for a successful ADS are:

* Planning
* Delivery
* Follow-up

### Planning

Before the ADS, establish the objectives you wish to achieve. Then, determine and prioritize the topics to cover. From this, create an agenda.

Collect any relevant artifacts that will assist in designing the architecture. This can include descriptions and diagrams of existing systems, as well as documentation on their roadmap. 

Identify the right people to attend the ADS. From your side, this should be a project owner and the subject-matter experts on the required technologies. From the customer's side, this should be the product owner and the architect who will work on the project. 

Decide when, where, and how to host the ADS. Ideally, this will be on-site and away from the customer's work environment. This is not always possible, so you may choose to host the ADS virtually or hold a hybrid event in which some attend in-person and others attend virtually. The important thing is that we remove the participants from potential distractions, so they can focus on the ADS.

Depending on the scope of the project, an ADS can last anywhere from 4 hours to 3 day.

Here is a sample agenda for a 2-day ADS:

Day 1:

| When| What |
| --- | --- |
| 9:00AM-9:15AM | Introduction |
| 9:15AM-Noon | Discovery Session: Review existing subsystems and requirements |
| Noon-1:00PM | Lunch |
| 1:00PM-3:00PM | Azure Technologies Walkthrough |
| 3:00PM-5:00PM | Architecture and Solution Design |

Day 2:

| When| What |
| --- | --- |
| 9:00AM-Noon | Architecture and Solution Design |
| Noon-1:00PM | Lunch |
| 1:00PM-3:00PM | Architecture and Solution Design |
| 3:00PM-4:30PM | Plan Next Steps |

### Delivery

On the day(s) of the ADS, we should strive to ???

#### Kickoff

Begin with a brief kickoff: Recap the purpose of the session; allow attendees to briefly introducte themselves; share the agenda; and explicitly state the objectives, roles, and responsibilities of team members.

#### Discovery

The goal of  this section is to understand the project goals and requirements - from a business and a technical perspective.

What is the current state of the application and the desired state? What is the business driver for this change? Are there any pain points?

Capture everything on a whiteboard and/or a notetaking application, such as OneNote.

Avoid discussing the solution at this point

#### Architecture and Solution Design

Design the future state of the application.

Discuss the components that can be used to implement the solution. How do these components communicate with one another? Use a whiteboard and/or whiteboard software to capture this.

For a Java application, consider the follwing Azure technologies:

* Azure Spring Apps
* Azure App Services
* Azure Container services
* Azure Kubernetes Service

There are likely to be other technologies, such as databases and queueing services that interact with the application.

Identify the non-functional requirements and determine how to handle them. These can include deployment, maintenance, high availability, disaster recovery, logging, and others.

Identify any risks in the proposed solution and provide guidance on mitigating those risks.

Define the architecture and design patterns that will be used in the solution.

Capture everything on a whiteboard and/or a notetaking application, such as OneNote.

Create a "Parking Lot" list for items that are out of scope.

### Follow-up

Take time at the end of the ADS to discuss the next steps. 

For the next meeting(s)?

* What is the cadence?
* Who should attend?
* What should be done by whom between now and then?

## Hackathon

Some customers will require upskilling on the technologies used in the solution. One method for upskilling is a "What the Hack" event. "What the Hack" is a set of challenge-based hackathons that can be hosted in-person or virtually via Microsoft Teams.

* [_What the Hack_ overview](https://microsoft.github.io/WhatTheHack/)
* [_What the Hack_ repo](https://github.com/Microsoft/WhatTheHack)

## POC

## Tech Briefing

The [Microsoft Azure Well Architected Framework](https://docs.microsoft.com/en-us/azure/architecture/framework/) provides guidance on building and migrating an application to Azure. The framework consists of five architectural "pillars": Reliability, Security, Cost Optimization, Operational Excellence, and Performance Efficiency.

### Reliability

Reliability is the ability to keep an application or service running, to anticipate failures, and to have a plan to recover quickly from those failures.

You can learn more about improving reliability in Azure applications [here](https://docs.microsoft.com/en-us/azure/architecture/framework/#reliability).

### Security

Security is an important pillar when architecting any application, whether or not it is in Azure. A key principle to keep in mind when designing your application is "Zero Trust" - never assume you can trust the person or account accessing your application.

You can learn more about improving security [here](https://docs.microsoft.com/en-us/azure/architecture/framework/#security).

### Cost Optimization

Azure resources can provide, but they cost money. This pillar helps you maximize the value for the price you are paying: Are you getting sufficient value for money outlayed and are there ways to save money, while still meeting your needs?

You can learn more about optimizing cost in Azure applications [here](https://docs.microsoft.com/en-us/azure/architecture/framework/#cost-optimization).

### Operational Excellence

Operational Excellence refers to the ability to deploy an application reliably and to verify that deployment.

You can learn more about improving operational excellence in Azure applications [here](https://docs.microsoft.com/en-us/azure/architecture/framework/#operational-excellence).

### Performance Efficiency

There are two ways to increase performance and capacity: Scaling up (increasing the power of your servers) and scaling out (increasing the number of nodes).

You can learn more about improving performance efficiency in Azure applications [here](https://docs.microsoft.com/en-us/azure/architecture/framework/#performance-efficiency).

## Solution Tech Review

(Assigned to Mike R)

## Build & Assist

(Assigned to Mike R)

## Roadmap Planning

(Assigned to Mike R)
