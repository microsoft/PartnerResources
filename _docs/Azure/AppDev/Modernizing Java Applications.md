---
layout: page
title: Modernizing Java Applications on Azure
description: A Plan for Modernizing Java Applications on Azure
updated: 2022-09-14
permalink: /azure/appdev/Modernizing-JavaApplications.md
tags:
- azure
- appdev
- technical resources 
- learning plan
- modernization
---

# Modernizing Java Applications on Azure (Draft)

* [Overview](#overview)
  * [Why Modernize?](#why)
  * [Costs vs Benefits](#costbenefit)
* [Envisioning](#envisioning)
* [Architecture Design Sessions](#ads)
* [Architecture Design Session for Service partners](#adspartner)
  * [Discover](#discover)
  * [Assess](#assess)
  * [Plan](#plan)
  * [Operationalize](#operationalize)
* [Architectural Design Session for ISVs](#adsisv)
* [Assessments](#assessments)
* [Upskilling](#upskilling)
  * [Documentation](#documentation)
  * [Labs](#labs)
  * [Hackathon](#hackathon)
  * [Other](#otherupskilling)
* [Proof of Concept](#poc)
* [Tech Briefing](#techbriefing)
* [Solution Technical Review](#techreview)
* [Roadmap Planning](#roadmap)

## <a name="overview"></a>Overview

Microsoft Azure contains native support for Java applications and the Java ecosystem. Java developers can continue using their favorite development environments, plugins, package managers, code repositories, and Life Cycle Management Tools, when deploying to Azure.

Many companies have successfully migrated their Java applications to Microsoft Azure, including the following:

* [Raley's](https://customers.microsoft.com/en-gb/story/1388620728739667057-raleys-uses-azure-spring-cloud-to-optimize-scale-and-drive-innovation)
* [Swiis Re](https://customers.microsoft.com/en-gb/story/1358540087031302788-swiss-re-accelerates-java-app-modernization-using-azure-spring-cloud)
* [Bosch](https://customers.microsoft.com/en-gb/story/1475571259638279673-bosch-delivers-supply-chain-efficiencies-java-azure)

This document describes an approach to modernizing Java applications to optimize the benefits of migrating an application to Azure.

### <a name="why"></a>Why Modernize?

Existing Java applications that run well on-premise may not be designed to take advantage of the flexibility and scalability that Microsoft Azure provides.

When considering migrating an application to Azure, it is useful to modernize the application and make it "cloud native" to better take advantage of the benefits of cloud computing. While a "lift and shift" approach - running your applications and data on virtual machines in the cloud - may work, it is likely to be inefficient. By architecting your application into distinct services that can be developed deployed and managed separately, you can increase the flexibility, maintainability, and scalability of your application. Microsoft Azure offers hundreds of managed services that free the developer from maintaining the underlying infrastructure of the application, allowing them to focus on solving business problems.

We have included links to resources recommended for partners looking to migrate their Java applications to Azure and will cover mainstream Java on Azure scenarios.  Readers can expect to learn how to migrate different types of Java applications to Azure, and understand how to build, deploy, and monitor those applications on Azure for their customers.

#### <a name="costbenefit"></a>Costs vs Benefits

Migrating an application to Azure provides potential cost savings. By renting compute and storage resources instead of buying them, we move from Capital Expenses to Operating Expenses. For volatile workloads, this can offer significant savings, as we don't need to pay for excess capacity when demand is low.

The [Azure Pricing Calculator](https://azure.microsoft.com/en-us/pricing/calculator/) allows you to estimate the cost of an application deployed to Azure.

##### Links

* [Enterprise Dev/Test Offer](https://azure.microsoft.com/en-us/offers/ms-azr-0148p/#:~:text=The%20Enterprise%20Dev/Test%20offer%20is,be%20accessed%20by%20any%20users.)
* [Total Economic Impact of Cloud Services](https://azure.microsoft.com/en-in/resources/the-total-economic-impact-of-microsoft-developer-tools-and-cloud-services/)
* [Azure Pricing Calculator](https://azure.microsoft.com/en-us/pricing/calculator/)
* [Cost Optimization video](https://docs.microsoft.com/en-us/azure/architecture/framework/#cost-optimization)
* [Cost Optimization documentation](https://docs.microsoft.com/en-us/azure/architecture/framework/cost/)

## <a name="envisioning"></a>Envisioning

An Envisioning Session is useful to exchange knowledge and determine if the project is appropriate for modernization.

The goals of an Envisioning Session are:

* Establish a clear understanding of business objectives
* Define how a potential solution would be used and how its performance should be measured
* Understand the capabilities of the development team and address any gasp
* Make sure all parties have the same understanding of the scope of the project
* Clearly communicate the next steps

At the end of the Envisioning Session, both parties should reach an agreement whether and when to proceed with the project.

## <a name="ads"></a>Architecture Design Sessions

A key part of any application modernization project is to conduct an Architecture Design Session (ADS) with the customer or partner. An ADS allows us to define and agree upon the architecture and scope of the application, making it easier to plan the development.

This is ideally done in-person to avoid distractions; however, it can also be accomplished successfully remotely or as a hybrid event with some attendees meeting in person and others participating virtually.

Below we cover ADS details for SI partners and for ISVs.

## <a name="adspartner"></a>Architecture Design Session for Services Partners

This guidance is specifically for Microsoft service partners (consulting companies, system integrators, managed service providers, Cloud Solution Providers, etc.) that are interested in modernizing their customer's Java workloads on Azure.

Microsoft provides resource for partners throughout the entire modernize journey. The journey is divided into distinct stages.

* Discover
* Assess
* Plan
* Modernize
* Operationalize

### <a name="discover"></a>Discover

* [App Service Migration Assistant Tool](https://appmigration.microsoft.com/)
* [Azure Database Migration Guide](https://datamigration.microsoft.com/)
* [Data Migration Service](https://docs.microsoft.com/en-us/azure/dms/)
* [Migrate Java Applications to Azure](https://docs.microsoft.com/en-us/azure/developer/java/migration/migration-overview)
* [How to Containerize and Deploy a Java app to Azure](https://www.youtube.com/watch?v=8BxcPngGaaM)

### <a name="assess"></a>Assess

* [Build migration plan with Azure Migrate](https://docs.microsoft.com/en-us/azure/migrate/concepts-migration-planning)
* [Azure App Service Migration Tool](https://azure.microsoft.com/en-us/services/app-service/migration-tools/)

### <a name="plan"></a>Plan

#### App Migration Planning

* [Migration Checklist for Azure App Service](https://azure.microsoft.com/en-us/blog/migration-checklist-when-moving-to-azure-app-service/)
* [Choosing an Azure compute service for your application](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-decision-tree?_lrsc=e623b82d-6c35-449e-9ff0-8cc81a0819e3)

The following Azure services can host a Java application. Consider which is appropriate for the current solution.

* Azure Spring Apps
* Azure App Service
* Azure Kubernetes Service

##### **Azure Spring Apps**

Azure Spring Apps is a Platform as a Service (PaaS) offering providing hosting, configuration, and Application Lifecycle Management, specifically designed for hosting Java Spring applications.

Read more about Azure Spring Apps [here](https://azure.microsoft.com/en-us/services/spring-apps/).

*More resources:*

* [Spring Boot to Azure Spring Apps](https://docs.microsoft.com/en-us/azure/developer/java/migration/migrate-spring-boot-to-azure-spring-cloud)
* [Tomcat to Azure Spring Apps](https://docs.microsoft.com/en-us/azure/developer/java/migration/migrate-tomcat-to-azure-spring-cloud)

##### **Azure App Service**

Azure App Service is a PaaS offering that hosts web applications, REST APIs, and mobile backends. Code can be deployed from a Java application or a number of other languages and platforms.

Read more about Azure App Service [here](https://docs.microsoft.com/en-us/azure/app-service/).

*More resources:*

* [Spring Boot to Azure App Service](https://docs.microsoft.com/en-us/azure/developer/java/migration/migrate-spring-boot-to-app-service)
* [Tomcat to Azure App Service](https://docs.microsoft.com/en-us/azure/developer/java/migration/migrate-tomcat-to-tomcat-app-service)
* [JBoss EAP to Azure App Service](https://docs.microsoft.com/en-us/azure/developer/java/migration/migrate-jboss-eap-to-jboss-eap-on-azure-app-service)
* [Configuring a Java app for Azure App Service](https://docs.microsoft.com/en-us/azure/app-service/configure-language-java?pivots=platform-linux)

##### **Azure Kubernetes Service**

Azure Kubernetes Service is a service that allows you to manage Kubernetes clusters within Azure. It supports any application that can run in a container, including Java applications.

Read more about Azure Kubernetes Service (AKS) [here](https://docs.microsoft.com/en-us/azure/aks/).

*More resources:*

* [Spring Boot to Azure Kubernetes Service](https://docs.microsoft.com/en-us/azure/developer/java/migration/migrate-spring-boot-to-azure-kubernetes-service)
* [Java web applications to Azure Kubernetes Service Learning Path](https://docs.microsoft.com/en-us/learn/modules/migrate-java-app-azure-kubernetes-service/)
* [Java Web App Containerization and Migration to Azure Kubernetes Service](https://docs.microsoft.com/en-us/azure/migrate/tutorial-app-containerization-java-kubernetes)

### <a name="modernize"></a>Modernize

#### Database Migration Planning

* [Choosing Your Database Migration Path](https://azure.microsoft.com/en-us/resources/choosing-your-database-migration-path-to-azure/)
* [SQL Migration](https://docs.microsoft.com/en-us/sql/sql-server/migrate/?view=sql-server-2017)

#### Migrate SQL open source DB to Azure DB

* [Deploy a Java EE/Jakarta EE application to App Service and bind it to Azure DB for MySQL](https://docs.microsoft.com/en-us/learn/modules/deploy-java-ee-app-to-jboss-app-service/)

#### Migrate NoSQL open source DB to CosmosDB

* [Java app to manage CosmosDB SQL Data Quickstart](https://docs.microsoft.com/en-us/azure/cosmos-db/sql/create-sql-api-java?tabs=sync)

#### Cloud Modernization

(Automate move from on-premise to Azure. What are considerations?)

#### App Modernization

#### Database Modernization

* [Cloud Journey Tracker](https://docs.microsoft.com/en-us/assessments/?mode=pre-assessment&amp;session=f13774ce-3324-46c7-9803-3b0298c49aed)
* [Solutions Assessment](https://www.microsoft.com/en-us/solutionassessments/solutionassessments.aspx?SilentAuth=1)

#### Deploy

* [Best Practices for Azure App Service](https://docs.microsoft.com/en-us/azure/app-service/app-service-best-practices)
* [Azure App Service Deployment Best Practices](https://docs.microsoft.com/en-us/azure/app-service/deploy-best-practices)
* [Highly Available Multi-Region Web Application on Azure](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/app-service-web-app/multi-region)
* [Microsoft Azure Well-Architected Framework](https://docs.microsoft.com/en-us/azure/architecture/framework/)
* [Cloud Adoption Framework](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/)
* [Best Practices for Cloud Applications](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)
* [Design Principles for Azure Applications](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/)
* [Application Performance Management (APM) on Azure](https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview)
* [Azure for Java developer documentation](https://docs.microsoft.com/en-us/azure/developer/java/?view=azure-java-stable)

### <a name="operationalize"></a>Operationalize

* [Azure Monitor for Java apps](https://docs.microsoft.com/en-us/azure/azure-monitor/app/java-in-process-agent)
* [Sign-in with Microsoft to a Java app](https://docs.microsoft.com/en-us/azure/active-directory/develop/web-app-quickstart?pivots=devlang-java)
* [Build Java apps with Azure DevOps](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/java?view=azure-devops)
* [Deploying Java to Azure App Service](https://docs.github.com/en/actions/deployment/deploying-to-your-cloud-provider/deploying-to-azure/deploying-java-to-azure-app-service)

### Azure Compete Scenarios

* [AWS to Azure services comparison](https://docs.microsoft.com/en-us/azure/architecture/aws-professional/services)
* [GCP to Azure services comparison](https://docs.microsoft.com/en-us/azure/architecture/gcp-professional/services)

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

Begin with a brief kickoff: Recap the purpose of the session; allow attendees to briefly introduce themselves; share the agenda; and explicitly state the objectives, roles, and responsibilities of team members.

#### Discovery

The goal of this section is to understand the project goals and requirements - from a business and a technical perspective.

What is the current state of the application and the desired state? What is the business driver for this change? Are there any pain points?

Capture everything on a whiteboard and/or a note-taking application, such as OneNote.

Avoid discussing the solution at this point

#### Architecture and Solution Design

Design the future state of the application.

Discuss the components that can be used to implement the solution. How do these components communicate with one another? Use a whiteboard and/or whiteboard software to capture this.

For a Java application, consider the following Azure technologies:

* Azure Spring Apps
* Azure App Services
* Azure Container services
* Azure Kubernetes Service

There are likely to be other technologies, such as databases and queuing services that interact with the application.

Identify the non-functional requirements and determine how to handle them. These can include deployment, maintenance, high availability, disaster recovery, logging, and others.

Identify any risks in the proposed solution and provide guidance on mitigating those risks.

Define the architecture and design patterns that will be used in the solution.

Capture everything on a whiteboard and/or a note-taking application, such as OneNote.

Create a "Parking Lot" list for items that are out of scope.

### Follow-up

Take time at the end of the ADS to discuss the next steps.

For the next meeting(s)?

* What is the cadence?
* Who should attend?
* What should be done by whom between now and then?

## <a name="assessments"></a>Assessments (Technical & Solution)

[Partner Readiness Resources for Azure Spring Apps](./Partner%20Readiness%20Resources%20for%20Spring%20Apps.md)

## <a name="upskilling"></a>Upskilling

Some partners will require upskilling on the technologies used in the solution. Microsoft and third parties offer a number of resources to assist in upskilling - with Java, with Azure, and with Java on Azure. Here are some options.

### <a name="documentation"></a>Documentation

* [Azure for Java developer documentation](https://docs.microsoft.com/en-us/azure/developer/java/)
* [Get help from Microsoft on Java](https://docs.microsoft.com/en-us/azure/developer/java/learning-resources/get-help)
* [Azure for Java quickstarts](https://docs.microsoft.com/en-us/azure/developer/java/quickstarts/)
* [Java on Azure](https://azure.microsoft.com/en-us/resources/developers/java/)
* [Introduction to Java on Azure Learning Path](https://docs.microsoft.com/en-us/learn/modules/intro-to-java-azure/)

### <a name="labs"></a>Labs

* [Azure Spring Cloud Training](https://github.com/CloudLabsAI-Azure/azure-spring-cloud-training)
* [Azure Immersion Workshop for Java](https://partner.microsoft.com/en-us/asset/collection/aiw-modernize-java-apps#/)

### <a name="hackathon"></a>Hackathons

One method for upskilling is a "What the Hack" event. "What the Hack" is a set of challenge-based hackathons that can be hosted in-person or virtually via Microsoft Teams.

* [*What the Hack* overview](https://microsoft.github.io/WhatTheHack/)
* [*What the Hack* repo](https://github.com/Microsoft/WhatTheHack)

Specific *What The Hack*s

* [Java on Azure App Service](https://microsoft.github.io/WhatTheHack/040-JavaOnAppService/)
* [App Modernization](https://microsoft.github.io/WhatTheHack/006-AppModernization/)

### <a name="otherupskilling"></a>Other Upskilling Resources

* Modernizing Java Apps and Data
  * [Part One: Introduction](https://www.codeproject.com/Articles/5324868/Modernizing-Java-Apps-and-Data-on-Azure-Part-One)
  * [Part Two: Migrating Data](https://www.codeproject.com/Articles/5324869/Modernizing-Java-Apps-and-Data-on-Azure-Part-Two-M)
  * [Part Three: Migrating to Azure App Service](https://www.codeproject.com/Articles/5324870/Modernizing-Java-Apps-and-Data-on-Azure-Part-Three)
  * [Part Four: Migrating to Azure Kubernetes Service](https://www.codeproject.com/Articles/5329178/Modernizing-Java-Apps-and-Data-on-Azure-Part-Four)
  * [Part Five: Data Modernization](https://www.codeproject.com/Articles/5329179/Modernizing-Java-Apps-and-Data-on-Azure-Part-Five)
  * [Part Six: Becoming Cloud Native](https://www.codeproject.com/Articles/5329180/Modernizing-Java-Apps-and-Data-on-Azure-Part-Six-B)
* [Java and Spring Boot Articles and Videos](https://davidgiard.com/java-and-spring-boot-articles-and-videos)

## <a name="poc"></a>Proof of Concept

We may have uncertainty if a technology is a good fit for our solution. In this case, a Proof of Concept (POC) will help. A Proof of Concept is a small application that demonstrates the capabilities of a technology in a given scenario. This helps us decide if the technology is appropriate for the solution, minimizing risk without investing inordinate time and money.

## <a name="techbriefing"></a>Tech Briefing

The [Microsoft Azure Well Architected Framework](https://docs.microsoft.com/en-us/azure/architecture/framework/) provides guidance on building and migrating an application to Azure. The framework consists of five architectural "pillars":

* Reliability
* Security
* Cost Optimization
* Operational Excellence
* Performance Efficiency

### Reliability

Reliability is the ability to keep an application or service running, to anticipate failures, and to have a plan to recover quickly from those failures.

You can learn more about improving reliability in Azure applications [here](https://docs.microsoft.com/en-us/azure/architecture/framework/#reliability).

### Security

Security is an important pillar when architecting any application, whether or not it is in Azure. A key principle to keep in mind when designing your application is "Zero Trust" - never assume you can trust the person or account accessing your application.

You can learn more about improving security [here](https://docs.microsoft.com/en-us/azure/architecture/framework/#security).

**More resources:**

* [Enable end-user authentication](https://docs.microsoft.com/en-us/azure/active-directory/develop/web-app-quickstart?pivots=devlang-java)
* [Microsoft Authentication Library](https://docs.microsoft.com/en-us/azure/active-directory/develop/migrate-adal-msal-java)
* [Manage app secrets](https://docs.microsoft.com/en-us/azure/key-vault/quick-create-java)

### Cost Optimization

Azure resources can provide, but they cost money. This pillar helps you maximize the value for the price you are paying: Are you getting sufficient value for money outlaid and are there ways to save money, while still meeting your needs?

You can learn more about optimizing cost in Azure applications [here](https://docs.microsoft.com/en-us/azure/architecture/framework/#cost-optimization).

### Operational Excellence

Operational Excellence refers to the ability to deploy an application reliably and to verify that deployment.

You can learn more about improving operational excellence in Azure applications [here](https://docs.microsoft.com/en-us/azure/architecture/framework/#operational-excellence).

### Performance Efficiency

There are two ways to increase performance and capacity: Scaling up (increasing the power of your servers) and scaling out (increasing the number of nodes).

You can learn more about improving performance efficiency in Azure applications [here](https://docs.microsoft.com/en-us/azure/architecture/framework/#performance-efficiency).

## <a name="techreview"></a>Solution Tech Review

Here is technical review guidance from the Microsoft US Partner Tech team.

The solution must contain at least one of these services listed below:

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

Additional Solution Services: Beyond the basic services, the solution may contain the below listed additional services, as part of the well architected solution.

* Application Gateway
* Azure Active Directory
* Azure Monitor
* Azure Storage
* Key Vault
* Security Center
* Traffic Manager

### Tech Review Requirements

* The partner should provide detailed explanation for one or more customer reference stories that clearly demonstrate Modernizing with Java.

* The partner should have sufficient staff with skills or certifications for Modernizing with Java.
* The partner’s staff should understand and leverage best practices as well as guidance and principles described in Application Architecture Center, Well-Architected Framework, Cloud Adoption Framework
* The partner's staff should understand and leverage App + Data Migration Tools – Azure Migrate, App Service Migration Assistant, Data Migration Assistant – for application migration projects.
* Earning the Advanced Specialization in "Modernization of Web Applications to Microsoft Azure" is recommended for a qualified partner. A partner is considered qualified for earning the advanced specialization if they meet both the criteria
  * Related competency: Must have an active Gold Cloud Platform Competency
  * Knowledge: Your organization must have at least six individuals who pass the following certifications:
    * One unique individual must pass Azure Administrator Associate certification AND
    * One unique individual must pass Azure Solutions Architect Expert certification AND
    * One unique individual must pass Azure DevOps Engineer Expert certification AND
    * One unique individual must pass Azure Security Engineer Associate certification AND
    * One unique individual must pass Azure Data Engineer Associate certification AND
    * One unique individual must pass Azure Developer Associate certification

### Best Practices

* HA: The partner should articulate how they ensure the solution is highly available for customers. They might implement at least one of the below services in the case of App Service Environment.
  * Availability Zones
  * Availability Sets
* Security: The partner should implement at least one or more of the below frameworks or methodologies for a secure solution architecture.
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
* BCDR: The partner should explain the solution SLA, RTO/RPO and backup practices.
* Governance: The partner should explain the different access control and governance policies practiced as part of solution implementation.
* IAM: The partner should explain how they implement identity, authentication and authorization in their solution. They should implement at least one of the below services.
  * Easy Auth
  * Azure Active Directory
  * Azure Active Directory B2C
  * Enterprise Applications
* DevOps: The partner should explain in detail on how they implement their DevOps strategy for easier repeatable code or infrastructure deployments. They should be familiar with the DevOps offerings with Azure and their implementations. Below is a list of such implementations.
  * Web Apps Deployment Slots
  * App Configuration
  * App Service Deployment Center
  * Git Integration
  * Containers (Linux + Windows)
* Observability: The partner must articulate their strategy for knowing the health of the solution. They must implement one or more of the below listed services.
  * Application Insights
  * Azure Monitor
  * Alerts
  * Log Analytics (Azure Monitor Logs)
  * Dashboards
  * Workbooks
  * KQL
  * Microsoft Sentinel
* Cost Effectiveness: The partner must be familiar with the scaling and compute options for all the Basic Solution Services listed above, to implement a cost-effective solution for the customer.
* Performance: The partner must articulate their strategy for high performing solution delivery. They should leverage at least one of the below:
  * Azure CDN
  * Azure Front Door
  * App Service Always On
  * Local Cache within App Configuration
  * Co-located deployments of DB with App Service in Azure Regions
* Compliance: The partner must explain the strategy implemented in the solution to comply with customer regulations. They may leverage one or more of the below:
  * Microsoft Defender for Cloud
  * App Service Environments (ASE)
  * Encryption
  * HTTPS

## <a name="roadmap"></a>Roadmap Planning

The following links provide information on the upcoming roadmap of Java on Microsoft Azure.

* [Microsoft for Java Developers Blog](https://devblogs.microsoft.com/java/tag/java/)
* [Azure Blog](https://azure.microsoft.com/en-us/blog)
* [Java and Azure GitHub Projects](https://github.com/search?q=azure+spring&ref=opensearch)
