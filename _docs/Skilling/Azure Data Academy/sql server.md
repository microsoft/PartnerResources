---
layout: page
title: Azure Data Academy
description: The Azure Data Academy is a series of presentations and hands-on material designed to upskill partners on data modernization in Microsoft Azure.
permalink: /skilling/azure-data-academy/sql
showbreadcrumb: true
updated: 2023-09-22
tags: 
- azure
- data, analytics, and ai
- azure data academy
- academy page
- sql server
---

# {{ page.title }}

Welcome to the Azure Data Academy content on Azure SQL and data integration. This section houses our content related to migration strategies, best practices, developer scenarios and operations topics related to Azure SQL Database, Azure SQL Managed Instance, and SQL Server running in an Azure Virtual Machine. We'll also include data integration related content.

{% include series.md 
    includetags="azure data academy|academy content|sql server" 
    includesecondtags="academy content|data integration" 
    includemethod="all" 
    sortfield="updated" sortorder="desc" showtags="true"
    visualstyle="normal"
%}

# SQL Server Migration to Azure 

## Pre-migration
This section includes information and details to help prepare for a migration. There are many resources to assist with the initial learning and skill development of Azure SQL capabilities. One resource to learn more about Azure SQL is the [Data Exposed](https://learn.microsoft.com/en-us/shows/data-exposed/) show. Additional references to specific Data Exposed shows are provided throughout the various sections below. In addition, [MS Learn](https://learn.microsoft.com/en-us/training/) has many learning modules on Azure SQL. References to specific MS Learn modules are also included in the sections below that are relevant to the specific topic.  

### Discovery
In any application and database migration, it is important to have a detailed understanding of the appliaction and database environement documented in order to evaluate target options and migration approaches. For the source system, examples of the information to collect and documenty include:

* Overall system size (CPU/RAM/IO subsystem), current usage, and versions (OS, database, application frameworks, etc)
* Architectural diagram showing application and database layout and interconnectivity. This includes cross database connectivity, ETL processes, and any feature usage such as transactional replication, read only secondaries, additional applications interfacing with the database.
* Security requirements: information on account types (for example, Azure AD), encryption requirements (such as TDE), audit requirements. 
* BCDR requirements: clustering, high availability, georeplication, backup and recovery, Long tern retention (LTR) etc. - having defined RPO (recovery point objective) and RTO (recovery time objective) numbers are essential.

#### Tools to assist with discovery
[Azure SQL Migration extension](https://learn.microsoft.com/en-us/azure/dms/migration-using-azure-data-studio?tabs=azure-sql-mi#known-issues-and-limitations) for [Azure Data Studio](https://learn.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver16&tabs=redhat-install%2Credhat-uninstall) will help you collect details of your environment. The Data Exposed show [Migrating to SQL: Get Started w/ Azure SQL Readiness Assessments & Migrations from ADS (Ep. 6)](https://learn.microsoft.com/en-us/shows/data-exposed/migrating-to-sql-get-started-with-azure-sql-readiness-assessments-and-migrations-from-ads) introduces the capabilities of Azure SQL Migration Extension. 

[Data Access Migration Toolkit](https://marketplace.visualstudio.com/items?itemName=ms-databasemigration.data-access-migration-toolkit) is a VS Code extension. This extension can be useful in scanning application source documents/code for data access pattern and used as input into the Azure SQL migration experience to evaluate your application code. 

### Assessment 
Using the information gathered during the discovery efforts, an assessment can be completed to determine the Azure SQL target options as well as any issues that may need to be addressed before a migration. 

### Determine Azure SQL platform

This [article](https://learn.microsoft.com/en-us/azure/azure-sql/azure-sql-iaas-vs-paas-what-is-overview?view=azuresql&viewFallbackFrom=sql-server-ver16) exaplains the capabilities of Azure SQL and the different options available. 

This [article](https://learn.microsoft.com/en-us/dotnet/azure/migration/sql) provides and overview of the Azure SQL options for migration.  

This is a training [resource](https://learn.microsoft.com/en-us/training/modules/deploy-paas-solutions-with-azure-sql/) to help with evauating and understanding the Azure SQL PaaS solutions. 

When considering Azure SQL Database the [resource management in Azure SQL Database](https://learn.microsoft.com/en-us/azure/azure-sql/database/resource-limits-logical-server?view=azuresql) which includes limitations to consider as well as the [Single database](https://learn.microsoft.com/en-us/azure/azure-sql/database/resource-limits-vcore-single-databases?view=azuresql) or [Elastic Pools](https://learn.microsoft.com/en-us/azure/azure-sql/database/resource-limits-vcore-single-databases?view=azuresql). 

The [Overview of Azure SQL Managed Instance resource limits](https://learn.microsoft.com/en-us/azure/azure-sql/managed-instance/resource-limits?view=azuresql#file-io-characteristics-in-general-purpose-tier) documentation page is a great resource for understanding capabilities, performance, and limitations to consider as you make you Azure SQL target desitnation.  In addition, understanding if an [Azure SQL Managed Instance pool (preview)](https://learn.microsoft.com/en-us/azure/azure-sql/managed-instance/instance-pools-overview?view=azuresql) would benefit your deployment should also be reviewed.   

This is a landing [page](https://learn.microsoft.com/en-us/data-migration/) for data migration scenario's.  

If the outcome of the assessment is to deploy to a SQL Server on an Azure SQL Database, this [resource](https://learn.microsoft.com/en-us/azure/azure-sql/migration-guides/database/sql-server-to-sql-database-overview?view=azuresql) provides comprehensive information on the migration process.  

If the outcome of the assessment is to deploy to a SQL Server on an Azure SQL Managed Instance, this [resource](https://learn.microsoft.com/en-us/azure/azure-sql/migration-guides/managed-instance/sql-server-to-managed-instance-overview?view=azuresql) provides comprehensive information on the migration process.  

If the outcome of the assessment is to deploy to a SQL Server on an Azure Virtual Machine, this [resource](https://learn.microsoft.com/en-us/azure/azure-sql/migration-guides/virtual-machines/sql-server-to-sql-on-azure-vm-individual-databases-guide?view=azuresql) provides comprehensive information on the deployment and configuration of an Azure SQL Server Virtual Machine. 

## Migration 
Migrations can be performed online or offline. The business requirements will help determine which option is best for the migration. 

### Azure Migrate
[Azure migrate](https://learn.microsoft.com/en-us/azure/migrate/migrate-services-overview) will help with the overall migration process. 

### Azure Data Studio
As noted above the [Azure SQL Migration extension](https://learn.microsoft.com/en-us/azure/dms/migration-using-azure-data-studio?tabs=azure-sql-mi#known-issues-and-limitations) for [Azure Data Studio](https://learn.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver16&tabs=redhat-install%2Credhat-uninstall) can be used to perform the migration. This is executed in combination with the [Azure Data Migration Service.](https://learn.microsoft.com/en-us/azure/dms/dms-overview) 

## Post-Migration

The following information includes steps and information for consideration after the migration is complete. 
https://learn.microsoft.com/en-us/sql/relational-databases/post-migration-validation-and-optimization-guide?view=sql-server-ver16

As the application and database transition to the Azure, there will be some activities that you will no longer performance, there will be some activities you will continue to perform as you have in the current environment, there will be some activities performed today that will transition in the wau they are performed, and there will be some new activities that you may not have performed in the current environment but will be essential now that the platform is in Azure. These sections below will describe these scenarios in the context of the [Azure Well-Architected Framework (WAF)](https://learn.microsoft.com/en-us/azure/architecture/framework/) 

### Well-Architected Framework (WAF) 

The [Azure Well-Architected Framework (WAF)](https://learn.microsoft.com/en-us/azure/architecture/framework/) consists of five pillars
* [Reliability](https://learn.microsoft.com/en-us/azure/well-architected/#reliability)
* [Security](https://learn.microsoft.com/en-us/azure/well-architected/#security)
* [Cost Optimization](https://learn.microsoft.com/en-us/azure/well-architected/#cost-optimization)
* [Operational Excellence](https://learn.microsoft.com/en-us/azure/well-architected/#operational-excellence)
* [Performance Efficiency](https://learn.microsoft.com/en-us/azure/well-architected/#performance-efficiency) 

The [Azure Well-Architected Framework (WAF)](https://learn.microsoft.com/en-us/azure/architecture/framework/) provides various [assessments](https://learn.microsoft.com/en-us/assessments/) that can be used to assist in determining areas of attention as you deploy your solution. 

#### [Reliability](https://learn.microsoft.com/en-us/azure/well-architected/#reliability)
Backup, Geo backup and restore, long term retention 
High availability considerations, cross region redundacy, Ready Only Secondaries (failover as well), monitoring and alterting 


#### [Security](https://learn.microsoft.com/en-us/azure/well-architected/#security)

Here is the MS Learn module [Configuring and manage SQL database security](https://learn.microsoft.com/en-us/training/modules/sql-database-security/)

Network configuration and isolation 

Security Baseline
https://techcommunity.microsoft.com/t5/azure-sql-blog/summary-of-the-2022-security-investments-in-azure-sql-and-sql/ba-p/3701607

Microsoft Defender - Security Defender

Role based access control (RBAC)

Managed service identities

Always Encrypted 

Azure Key Vault 

Purview – Information Classification 

#### [Cost Optimization](https://learn.microsoft.com/en-us/azure/well-architected/#cost-optimization)

The ability to monitor and analyze spend over time is important to ensure you are optimizing your resource utilization and cost. Advantages of Azure include the ability to scale up or down as needed, leverage serverless or pause and resume options to optimize resource utilization and cost. As well as scaling considerations and resource management that may be different for various scenarios such as development, test, and production evironments.

You can read the article [Optimize Cost in Azure SQL Managed Instance](https://techcommunity.microsoft.com/t5/azure-sql-blog/optimize-costs-in-azure-sql-managed-instance/ba-p/3792571) for more inforation about the cost optimization considerations.

[Azure cost management](https://azure.microsoft.com/en-us/products/cost-management/) 

[Azure advisor](https://learn.microsoft.com/en-us/azure/advisor/advisor-overview) 

Azure SQL Database has [serverless](https://learn.microsoft.com/en-us/azure/azure-sql/database/serverless-tier-overview?view=azuresql&tabs=general-purpose) options may be a useful way to manage costs. 
 
Azure SQL Managed Instance introduced the ability to start and stop an instance. In this short [video](https://www.youtube.com/watch?v=94-QCey596o) you will a demonstration of Azure SQL Managed Instance Start and Stop capabilities.
        
#### [Operational Excellence](https://learn.microsoft.com/en-us/azure/well-architected/#operational-excellence)

[SQL Server best practices assessment (BPA)](https://techcommunity.microsoft.com/t5/sql-server-blog/best-practices-assessment-arc-enabled-sql-server/ba-p/3715776 )

[Maintence windows](https://learn.microsoft.com/en-us/azure/azure-sql/database/maintenance-window?view=azuresql)

##### Azure Data Studio – 

Azure Data Studio has the ability to create [notebooks](https://learn.microsoft.com/en-us/sql/azure-data-studio/notebooks/notebooks-guidance?view=sql-server-ver16) which are usful for creating Troubleshooting Guides (TSG’s)  

##### DevOps
Azure Data studio - [Database projects](https://learn.microsoft.com/en-us/sql/azure-data-studio/extensions/sql-database-project-extension-getting-started?view=sql-server-ver16)

Azure SQL Database [Local development experience](https://learn.microsoft.com/en-us/azure/azure-sql/database/local-dev-experience-overview?view=azuresql)

VS Code [SQL Server Extension](https://learn.microsoft.com/en-us/sql/tools/visual-studio-code/mssql-extensions?view=sql-server-ver16) 

Microsoft SQL Server Data-Tier Application Framework DacFx
[SqlPackage](https://learn.microsoft.com/en-us/sql/tools/sqlpackage/sqlpackage?view=sql-server-ver16) is a command-line tool used for database development activities. 

Automation and Infrastructure as code using PowerShell or [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/azure-cli-reference-for-sql) 

#### [Performance Efficiency](https://learn.microsoft.com/en-us/azure/well-architected/#performance-efficiency)
In addition to ensure the application is performing to the requirements and needs of the business, it is important to ensure that the database is performing efficiently to assist with overal resource utilization and cost optimization. Azure provides additional tools and capabilities along side the tools you are familiar with from SQL Server, but Azure also adds additional considerations to know and manage to ensure the database is operating in the most performant way. 

Azure Portal

Azure Monitor

Query Store

Intelligent Query Processing (IQP)  

Automatic tuning 

Columnstore

Non Clustered Columnstore (NCCS)

Database compatibility level 

Data virtualization 

## Modernization 
This section includes information related to topics that you can consider to enhance or expand the capabilities of your application from functionality within Azure SQL. 

The Ledger capability is available within Azure SQL Database and SQL Server 2022. 

In-memory OLTP

Temporal tables

Analytical scenarios such as HTAP and Azure Synapse Link for SQL.  

Azure SQL Database introduced the ability to call REST and functions.  

Link for Managed Instance 
   
### Azure SQL Server Virtual Machine
IaaS Extension
https://techcommunity.microsoft.com/t5/azure-sql-blog/2022-a-year-of-unparalleled-innovation-in-azure-sql-managed/ba-p/3676757


## Feedback

Have a content session recommendation or general feedback? Here's how to give it:
* Use of [feedback form to let us know](https://aka.ms/ada-feedback)
* Create a [documentation issue in GitHub](https://github.com/microsoft/PartnerResources/issues/new?labels=feedback&title=Azure%20Data%20Academy%20feedback) to begin a conversation.

Not sure which to use? To fire off a quick suggestion, use the Office Form. It's quick and anonymous. If you'd like to start a dialog on a topic, use the Issues in GitHub with the 'feedback' label.

## Contributions

We welcome contributors to this project. Please use the GitHub links near the upper right and consider submitting pull requests or filing issues as needed.
