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
(See slide 46 of Taxonomy deck)

#### App Migration Planning

<!-- * [Architecture, Migration Process, Components](https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/articles/net-app-modernization) -->
<!-- * [Migrate, modernize .NET applications with Azure](https://techcommunity.microsoft.com/t5/apps-on-azure/migrate-modernize-net-applications-with-azure/ba-p/1696499) -->
* [Migration Checklist for Azure App Service](https://azure.microsoft.com/en-us/blog/migration-checklist-when-moving-to-azure-app-service/)
<!-- * [Apps Migration Considerations](https://docs.microsoft.com/en-us/dotnet/azure/migration/app-service) -->
* [Choosing an Azure compute service for your application](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-decision-tree?_lrsc=e623b82d-6c35-449e-9ff0-8cc81a0819e3)

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

## Hackathon

"What the Hack" is a set of challenge-based hackathons that can be hosted in-person or virtually via Microsoft Teams.

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
