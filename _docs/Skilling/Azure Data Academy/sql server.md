---
layout: page
title: Azure Data Academy
description: The Azure Data Academy is a series of presentations and hands-on material designed to upskill partners on data modernization in Microsoft Azure.
permalink: /skilling/azure-data-academy/sql
showbreadcrumb: false
---

# {{ page.title }}

Welcome to the Azure Data Academy content on Azure SQL. This section houses our content related to migration strategies, best practices, developer scenarios and operations topics related to Azure SQL Database, Azure SQL Managed Instance, and SQL Server running in an Azure Virtual Machine.

{% include series.md 
    includetags="azure data academy|sql server" includemethod="all" 
    sortfield="updated" sortorder="desc" showtags="true"
    visualstyle="normal"
%}

# SQL Server Migration to Azure 

## Pre-migration
This section includes information and details to help prepare for a migration. There are many resources to assist with the initial learning and skill development of the Azure SQL capabilities. One resource to learn more about Azure SQL in the [Data Exposed](https://learn.microsoft.com/en-us/shows/data-exposed/) show. Additional references to specific shows are throughout the various sections below. In addition, [MS Learn](https://learn.microsoft.com/en-us/training/) has many modules on Azure SQL. References to specific MS Learn modules are included in the sections below that are relevant to the specific topic.  

### Discovery
In any application and database migration, it is important to have a detailed understanding of the appliaction and database environement documented in order to evaluate target options and migration approaches. For the source system, examples of the information to collect and documenty include:

* Overall system size (CPU/RAM/IO subsystem), current usage, and versions (OS, database, application frameworks, etc)
* Architectural diagram showing application and database layout and interconnectivity. This includes cross database connectivity, ETL processes, and any feature usage such as transactional replication, read only secondaries, additional applications interfacing with the database.
* Security requirements: information on account types (for example, Azure AD), encryption requirements (such as TDE), audit requirements. 
* BCDR requirements: clustering, high availability, georeplication, backup and recovery, Long tern retention (LTR) etc. - having defined RPO (recovery point objective) and RTO (recovery time objective) numbers are essential.

#### Tools to assist with discovery
[Azure SQL Migration extension](https://learn.microsoft.com/en-us/azure/dms/migration-using-azure-data-studio?tabs=azure-sql-mi#known-issues-and-limitations) for Azure Data Studio will help you collect details of your environment. The Data Exposed show [Migrating to SQL: Get Started w/ Azure SQL Readiness Assessments & Migrations from ADS (Ep. 6)](https://learn.microsoft.com/en-us/shows/data-exposed/migrating-to-sql-get-started-with-azure-sql-readiness-assessments-and-migrations-from-ads) introduces the capabilities of Azure SQL Migration Extension. 

[Data Access Migration Toolkit](https://marketplace.visualstudio.com/items?itemName=ms-databasemigration.data-access-migration-toolkit) (Tooling)
This tool can be useful in scanning application source documents/code for data access pattern

With this information, options can be evaluated for both cost and technical feasibility. For example, a large server with many dependent databases may be a better fit for Azure SQL Database Managed Instance, whereas a server with dozens or hundreds of independent databases may be a better fit for Azure SQL Database.

### Assessment 
Using the information gathered during the discovery efforts, an assessment can be completed to determine the Azure SQL target options as well as any issues that may need to be addressed before a migration. 

### Determine Azure SQL platform

This [article](https://learn.microsoft.com/en-us/azure/azure-sql/azure-sql-iaas-vs-paas-what-is-overview?view=azuresql&viewFallbackFrom=sql-server-ver16) exaplains the capabilities of Azure SQL and the different options available. 

This [article](https://learn.microsoft.com/en-us/dotnet/azure/migration/sql) provides and overview of the Azure SQL options for migration.  

This is a training [resource](https://learn.microsoft.com/en-us/training/modules/deploy-paas-solutions-with-azure-sql/) to help with evauating and understanding the Azure SQL PaaS solutions. 

This is a landing [page](https://learn.microsoft.com/en-us/data-migration/) for data migration scenario's.  

If the outcome of the assessment is to deploy to a SQL Server on an Azure SQL Database, this [resource](https://learn.microsoft.com/en-us/azure/azure-sql/migration-guides/database/sql-server-to-sql-database-overview?view=azuresql) provides comprehensive information on the migration process.  

If the outcome of the assessment is to deploy to a SQL Server on an Azure SQL Managed Instance, this [resource](https://learn.microsoft.com/en-us/azure/azure-sql/migration-guides/managed-instance/sql-server-to-managed-instance-overview?view=azuresql) provides comprehensive information on the migration process.  

If the outcome of the assessment is to deploy to a SQL Server on an Azure Virtual Machine, this [resource](https://learn.microsoft.com/en-us/azure/azure-sql/migration-guides/virtual-machines/sql-server-to-sql-on-azure-vm-individual-databases-guide?view=azuresql) provides comprehensive information on the deployment and configuration of an Azure SQL Server Virtual Machine. 

## Migration 
Migrations can be performed online or offline. The business requirements will help determine which option is best for the migration. 

### Azure Migrate

### Azure Data Studio
As noted above the [Azure SQL Migration extension](https://learn.microsoft.com/en-us/azure/dms/migration-using-azure-data-studio?tabs=azure-sql-mi#known-issues-and-limitations) for Azure Data Studio can be used to perform the migration. This is executed in combination with the [Azure Data Migration Service.](https://learn.microsoft.com/en-us/azure/dms/dms-overview) 

## Post-Migration

The following information includes steps and information for consideration after the migration is complete. 
https://learn.microsoft.com/en-us/sql/relational-databases/post-migration-validation-and-optimization-guide?view=sql-server-ver16

### Well-Architected Framework (WAF) 

The Azure Well-Architected Framework (WAF) consists of five pillars
* Reliability
* Security
* Cost Optimization
* Operational Excellence
* Performance Efficiency 

Detailed information on the Well-Architected Framework (WAF) can be found here:
https://learn.microsoft.com/en-us/azure/architecture/framework/

#### Reliabilty
Backup, Geo backup and restore, long term retention 
High availability considerations, cross region redundacy, Ready Only Secondaries (failover as well), monitoring and alterting 


#### Security

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

#### Cost Optimization
Azure cost management 
[Azure advisor](https://learn.microsoft.com/en-us/azure/advisor/advisor-overview) 

Scaling considerations such as serverless options, pause \ resume options help with the management of cost for development, test, and production evironments. Azure SQL Database has serverless options. Azure SQL Managed Instance introduced the ability to start and stop an instance. 
        
#### Operational Excellence

[SQL Server best practices assessment (BPA)](https://techcommunity.microsoft.com/t5/sql-server-blog/best-practices-assessment-arc-enabled-sql-server/ba-p/3715776 )

[Maintence windows](https://learn.microsoft.com/en-us/azure/azure-sql/database/maintenance-window?view=azuresql)

##### Azure Data Studio – 

Azure Data Studio has the ability to create [notebooks](https://learn.microsoft.com/en-us/sql/azure-data-studio/notebooks/notebooks-guidance?view=sql-server-ver16) which are usful for creating Troubleshooting Guides (TSG’s)  

##### DevOps
Azure Data studio - [Database projects](https://learn.microsoft.com/en-us/sql/azure-data-studio/extensions/sql-database-project-extension-getting-started?view=sql-server-ver16)

Azure SQL Database [Local development experience](https://learn.microsoft.com/en-us/azure/azure-sql/database/local-dev-experience-overview?view=azuresql)

VS Code SQL projects

Microsoft SQL Server Data-Tier Application Framework DacFx
[SqlPackage](https://learn.microsoft.com/en-us/sql/tools/sqlpackage/sqlpackage?view=sql-server-ver16) is a command-line tool used for database development activities. 

Automation and Infrastructure as code using PowerShell or Azure CLI 

#### Performance Efficiency
Azure Portal

Azure Monitor

Query Store

Intelligent Query Processing (IQP)  

Columnstore

Non Clustered Columnstore (NCCS)

Database compatibility level 

Automatic tuning 

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
