---
layout: page
title: Modernizing Java Applications
description: Modernizing Java Applications on Azure
updated: 2024-01-16
permalink: /skilling/developer-velocity-academy/resources/modernizing-javaapplications
tags:
- learning plan
- azure
- appdev
- java
- modernization
---

# Modernizing Java Applications on Azure

## Table of Contents

* [Overview](#overview)
  * [Why Modernize?](#why)
  * [Costs vs Benefits](#costbenefit)
* [Envisioning](#envisioning)
* [Architecture Design Sessions](#ads)
* [Architecture Design Session for Service Partners](#adspartner)
  * [Discover](#discover)
  * [Assess](#assess)
  * [Plan](#plan)
  * [Operationalize](#operationalize)
* [Architectural Design Session for ISVs](#adsisv)
* [Upskilling](#upskilling)
  * [Documentation](#documentation)
* [Proof of Concept](#poc)
* [Tech Briefing](#techbriefing)
* [Solution Technical Review](#techreview)

## <a name="overview"></a>Overview

Microsoft Azure contains native support for Java applications and the Java ecosystem. Java developers can continue using their favorite development environments, plugins, package managers, code repositories, and Life Cycle Management Tools, when deploying to Azure.

### <a name="why"></a>Why Modernize?

Existing Java applications that run well on-premise may not be designed to take advantage of the flexibility and scalability that Microsoft Azure provides.

When considering migrating an application to Azure, it is useful to modernize the application and make it "cloud native" to better take advantage of the benefits of cloud computing. While a "lift and shift" approach may work, it is likely to be inefficient.

By architecting your application into distinct services that can be developed, deployed, and managed separately, you can increase the flexibility, maintainability, and scalability of your application. Microsoft Azure offers hundreds of managed services that free the developer from maintaining the underlying infrastructure of the application, allowing them to focus on solving business problems.

### <a name="costbenefit"></a>Costs vs Benefits

Migrating an application to Azure provides cost savings. By renting compute and storage resources instead of buying them, we move from Capital Expenses to Operating Expenses. For volatile workloads, this can offer significant savings, as we don't need to pay for excess capacity when demand is low.

The **[Azure Pricing Calculator](https://azure.microsoft.com/en-us/pricing/calculator/)** allows you to estimate the cost of an application deployed to Azure.

#### Useful Links

* [Enterprise Dev/Test Offer](https://azure.microsoft.com/en-us/offers/ms-azr-0148p/#:~:text=The%20Enterprise%20Dev/Test%20offer%20is,be%20accessed%20by%20any%20users.)
* [Cost Optimization Documentation](https://docs.microsoft.com/en-us/azure/architecture/framework/cost/)

## <a name="envisioning"></a>Envisioning

An Envisioning Session is useful to exchange knowledge and determine if the project is appropriate for modernization.

The goals of an Envisioning Session are:

* Establish a clear understanding of business objectives
* Define how a potential solution would be used and how its performance should be measured
* Understand the capabilities of the development team and address any gaps
* Make sure all parties have the same understanding of the scope of the project
* Clearly communicate the next steps

At the end of the Envisioning Session, both parties should reach an agreement whether and when to proceed with the project.

## <a name="ads"></a>Architecture Design Sessions

A key part of any application modernization project is to conduct an Architecture Design Session (ADS) with the customer or partner. An ADS allows us to define and agree upon the architecture and scope of the application, making it easier to plan the development.

This is ideally done in person to avoid distractions; however, it can also be accomplished successfully remotely or as a hybrid event with some attendees meeting in-person and others participating virtually.

Below we cover ADS details for SI partners and for ISVs.

## <a name="adspartner"></a>Architecture Design Session for Services Partners

This guidance is specifically for Microsoft service partners (Ex. consulting companies, system integrators, managed service providers, Cloud Solution Providers, etc.) that are interested in modernizing their customer's Java workloads on Azure.

Microsoft provides resources for partners throughout the entire modernize journey. The journey is divided into distinct stages.

* Discover
* Assess
* Plan
* Modernize
* Operationalize

### <a name="discover"></a>Discover

* [Azure Database Migration Guides](https://datamigration.microsoft.com/)
* [Data Migration Service](https://docs.microsoft.com/en-us/azure/dms/)
* [Migrate Java Applications to Azure](https://docs.microsoft.com/en-us/azure/developer/java/migration/migration-overview)
* [How to Containerize & Deploy a Java App to Azure](https://www.youtube.com/watch?v=8BxcPngGaaM)

### <a name="assess"></a>Assess

* [Build Migration Plan with Azure Migrate](https://docs.microsoft.com/en-us/azure/migrate/concepts-migration-planning)

### <a name="plan"></a>Plan

The following Azure services can host a Java application. Consider which is appropriate for the current solution.

* Azure Spring Apps
* Azure App Service
* Azure Kubernetes Service

**[This document](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-decision-tree?_lrsc=e623b82d-6c35-449e-9ff0-8cc81a0819e3)** contrasts these services and provides some guidance on choosing the appropriate service.

#### **Azure Spring Apps**

Azure Spring Apps is a Platform as a Service (PaaS) offering providing hosting, configuration, and Application Lifecycle Management, specifically designed for hosting Java Spring applications.

Read more about Azure Spring Apps **[here](https://azure.microsoft.com/en-us/services/spring-apps/).**

*More resources:*

* [Spring Boot to Azure Spring Apps](https://docs.microsoft.com/en-us/azure/developer/java/migration/migrate-spring-boot-to-azure-spring-cloud)
* [Tomcat to Azure Spring Apps](https://docs.microsoft.com/en-us/azure/developer/java/migration/migrate-tomcat-to-azure-spring-cloud)

#### **Azure App Service**

Azure App Service is a Platform as a Service (PaaS) offering that hosts web applications, REST APIs, and mobile backends. Code can be deployed from a Java application or a number of other languages and platforms.

Read more about Azure App Service **[here](https://docs.microsoft.com/en-us/azure/app-service/).**

*More resources:*

* [JBoss EAP to Azure App Service](https://docs.microsoft.com/en-us/azure/developer/java/migration/migrate-jboss-eap-to-jboss-eap-on-azure-app-service)
* [Configuring a Java App for Azure App Service](https://docs.microsoft.com/en-us/azure/app-service/configure-language-java?pivots=platform-linux)

#### **Azure Kubernetes Service**

Azure Kubernetes Service is a service that allows you to manage Kubernetes clusters within Azure. It supports any application that can run in a container, including Java applications.

Read more about Azure Kubernetes Service (AKS) **[here](https://docs.microsoft.com/en-us/azure/aks/).**

*More resources:*

* [Migrate Java Web Apps to Azure Kubernetes Service (AKS)](https://docs.microsoft.com/en-us/learn/modules/migrate-java-app-azure-kubernetes-service/)
* [Java Web App Containerization & Migration to Azure Kubernetes Service (AKS)](https://docs.microsoft.com/en-us/azure/migrate/tutorial-app-containerization-java-kubernetes)

### <a name="modernize"></a>Modernize

#### Database Migration Planning

* [SQL Migration](https://docs.microsoft.com/en-us/sql/sql-server/migrate/?view=sql-server-2017)

#### Migrate SQL to Azure

* [Deploy a Java EE (Jakarta EE) App to Azure](https://docs.microsoft.com/en-us/learn/modules/deploy-java-ee-app-to-jboss-app-service/)

#### Migrate NoSQL to CosmosDB

* [Azure Cosmos DB for NoSQL](https://docs.microsoft.com/en-us/azure/cosmos-db/sql/create-sql-api-java?tabs=sync)

#### Database Modernization

* [Solutions Assessments](https://www.microsoft.com/en-us/solutionassessments/solutionassessments.aspx?SilentAuth=1)

#### Deploy

* [Best Practices for Azure App Service](https://docs.microsoft.com/en-us/azure/app-service/app-service-best-practices)
* [Azure App Service Deployment Best Practices](https://docs.microsoft.com/en-us/azure/app-service/deploy-best-practices)
* [Highly Available Multi-Region Web Apps on Azure](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/app-service-web-app/multi-region)
* [Design Principles for Azure Applications](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/)
* [Application Insights on Azure](https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview)

### <a name="operationalize"></a>Operationalize

* [Build Java Apps with Azure DevOps](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/java?view=azure-devops)
* [Deploying Java to Azure App Service](https://docs.github.com/en/actions/deployment/deploying-to-your-cloud-provider/deploying-to-azure/deploying-java-to-azure-app-service)

## <a name="adsisv"></a>Architecture Design Session for ISVs

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

Identify the right people to attend the ADS. From your side, this should be the **project owner** and the subject-matter experts on the required technologies. From the customer's side, this should be the **product owner** and the architect(s) who will work on the project.

Decide when, where, and how to host the ADS. Ideally, this will be on-site and away from the customer's work environment. This is not always possible, so you may choose to host the ADS virtually or hold a hybrid event in which some attend in-person and others attend virtually.

Depending on the scope of the project, an ADS can last anywhere from 4 hours to 3 days.

Here is a sample agenda for a 2-day ADS:

**Day #1:**

| When| What |
| --- | --- |
| 9:00AM-9:15AM | Introduction |
| 9:15AM-Noon | Discovery Session: Review existing systems and requirements |
| Noon-1:00PM | Lunch |
| 1:00PM-3:00PM | Azure Technologies |
| 3:00PM-5:00PM | Architecture and Solution Design |

**Day #2:**

| When| What |
| --- | --- |
| 9:00AM-Noon | Architecture and Solution Design |
| Noon-1:00PM | Lunch |
| 1:00PM-3:00PM | Architecture and Solution Design |
| 3:00PM-4:30PM | Plan Next Steps |

## Delivery

Begin with a brief kickoff: Recap the purpose of the session; allow attendees to briefly introduce themselves; share the agenda; and explicitly state the objectives, roles, and responsibilities of team members.

#### Discovery

What is the current state of the application and the desired state? What is the business driver for this change? Are there any pain points? Capture everything on a whiteboard and/or a note-taking application, such as OneNote. Avoid discussing the solution at this point.

#### Architecture and Solution Design

Design the future state of the application.

Discuss the components that can be used to implement the solution. How do these components communicate with one another? Use a whiteboard and/or whiteboard software to capture this.

For a Java application, consider the following Azure technologies:

* Azure Spring Apps
* Azure App Services
* Azure Container services
* Azure Kubernetes Service

#### Steps

1. There are likely to be other technologies, such as databases and queuing services that interact with the application.
2. Identify the non-functional requirements and determine how to handle them (Ex. deployment, maintenance, availability, disaster recovery, logging, etc.)
3. Identify any risks in the proposed solution and provide guidance on mitigating those risks.
4. Define the architecture and design patterns that will be used in the solution.
5. Capture everything on a whiteboard and/or a note-taking application, such as OneNote.
6. Create a "Parking Lot" list for items that are out of scope.

### Follow-up

Take time at the end of the ADS to discuss the next steps.

For the next meeting(s)?:

* What is the cadence?
* Who should attend?
* What should be done by whom between now and then?

## <a name="upskilling"></a>Upskilling

Some partners will require upskilling on the technologies used in the solution. Microsoft and 3rd-parties offer a number of resources to assist in upskilling.

### <a name="documentation"></a>Documentation

* [Azure for Java Developer Documentation](https://docs.microsoft.com/en-us/azure/developer/java/)
* [Get Help from Microsoft on Java](https://docs.microsoft.com/en-us/azure/developer/java/learning-resources/get-help)
* [Azure for Java QuickStarts](https://docs.microsoft.com/en-us/azure/developer/java/quickstarts/)
* [Introduction to Java on Azure](https://docs.microsoft.com/en-us/learn/modules/intro-to-java-azure/)
* [Java and Spring Boot Articles & Videos](https://davidgiard.com/java-and-spring-boot-articles-and-videos)

## <a name="poc"></a>Proof of Concept

We may be uncertain if a technology is a good fit for our solution. In this case, a Proof of Concept (POC) will help. A Proof of Concept is a small application that demonstrates the capabilities of a technology in a given scenario. This helps us decide if the technology is appropriate for the solution, minimizing risk without investing inordinate time and money.

## <a name="techbriefing"></a>Tech Briefing

The **[Microsoft Azure Well Architected Framework](https://docs.microsoft.com/en-us/azure/architecture/framework/)** provides guidance on building and migrating an application to Azure. The framework consists of five architectural "pillars":

* Reliability
* Security
* Cost Optimization
* Operational Excellence
* Performance Efficiency

## <a name="techreview"></a>Solution Tech Review

Here is technical review guidance from the Microsoft US Partner Tech Team.

The solution must contain at least one of the services listed below:

* API Management
* App Service
* Azure Container Instance
* Azure Spring Apps
* Azure SQL DB
* Event Grid
* Functions
* Logic Apps
* Media Services
* Red Hat OpenShift
* Service Bus
* Signal R

Additional Solution Services:

* Application Gateway
* Azure Active Directory (AAD)
* Azure Monitor
* Azure Storage
* Key Vault
* Security Center
* Traffic Manager

### Tech Review Requirements

The partner should provide detailed explanations for one or more customer reference stories that clearly demonstrate Modernizing with Java.

* The partner should have sufficient staff with skills or certifications for Modernizing with Java
* The partner’s staff should understand and leverage best practices as well as guidance and principles described in the Application Architecture Center, Azure Well-Architected Framework, and Cloud Adoption Framework
* The partner's staff should understand and leverage App and Data Migration Tools (Ex. Azure Migrate, App Service Migration Assistant, Data Migration Assistant)

### Best Practices

**High Availability (HA):** The partner should articulate how they ensure the solution is highly available for customers. They might implement at least one of the services below in the case of App Service Environment:

  * Availability Zones
  * Availability Sets

**Security:** The partner should implement at least one or more of the below frameworks or methodologies for a secure solution architecture:

  * Azure Security Benchmark
  * Security Pillar of the Well Architected Framework
  * Easy Auth
  * HTTPS
  * Service Endpoints
  * Private Endpoints
  * VNET Integration
  * App Service Environments
  * Allow Lists
  * Authentication
  * Key Vault
  * App Configuration
  * Application Gateway
  * Microsoft Defender for Cloud
  * Microsoft Sentinel

**Business Continuity and Disaster Recovery (BCDR):** The partner should explain the solution SLA and RTO/RPO.

**Governance:** The partner should explain the different access control and governance policies practiced as part of solution implementation.

**Identity Access Management (IAM):** The partner should explain how they implement identity, authentication, and authorization in their solution. They should implement at least one of the services below:

  * Easy Auth
  * Azure Active Directory
  * Azure Active Directory B2C
  * Enterprise Applications

**DevOps**: The partner should explain in detail how they implement their DevOps strategy for easier repeatable code and/or infrastructure deployments. They should be familiar with the DevOps offerings within Azure and their implementations. Below is a list of such implementations:

  * Web Apps Deployment Slots
  * App Configuration
  * App Service Deployment Center
  * Git Integration
  * Containers (Linux + Windows)

**Observability**: The partner must articulate their strategy for knowing the health of the solution. They must implement one or more of the services listed below:

  * Application Insights
  * Azure Monitor
  * Alerts
  * Log Analytics
  * Dashboards
  * Workbooks
  * KQL
  * Microsoft Sentinel

**Cost Effectiveness**: The partner must be familiar with scaling and compute options to implement a cost-effective solution for the customer.

**Performance**: The partner must articulate their strategy for high performing solution delivery. They should leverage at least one of the following:

  * Azure CDN
  * Azure Front Door
  * App Service Always On
  * Local Cache within App Configuration
  * Co-located Deployments of DB with App Service in Azure Regions

**Compliance**: The partner must explain the strategy implemented in the solution to comply with customer regulations. They may leverage one or more of the below:

  * Microsoft Defender for Cloud
  * App Service Environments (ASE)
  * Encryption
  * HTTPS