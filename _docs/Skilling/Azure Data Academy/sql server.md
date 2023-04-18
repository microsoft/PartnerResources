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
### Discovery
In any application and database migration, it is important to have a detailed understanding of the appliaction and database environement documented in order to evaluate target options and migration approaches. For the source system, examples of the information to collect and documenty include:

* Overall system size (CPU/RAM/IO subsystem), current usage, and versions (OS, database, application frameworks, etc)
* Architectural diagram showing application and database layout and interconnectivity. This includes cross database connectivity, ETL processes, and any feature usage such as transactional replication, read only secondaries, additional applications interfacing with the database.
* Security requirements: information on account types (for example, Azure AD), encryption requirements (such as TDE), audit requirements. 
* BCDR requirements: clustering, high availability, georeplication, backup and recovery, Long tern retention (LTR) etc. - having defined RPO (recovery point objective) and RTO (recovery time objective) numbers are essential.

[Data Access Migration Toolkit](https://marketplace.visualstudio.com/items?itemName=ms-databasemigration.data-access-migration-toolkit) (Tooling)
This tool can be useful in scanning application source documents/code for data access pattern

With this information, options can be evaluated for both cost and technical feasibility. For example, a large server with many interconnected databases will likely be a better fit for Azure SQL Database Managed Instance, whereas a server with dozens or hundreds of independent databases will likely be a better fit for Azure SQL Database (singleton) with Elastic Pools.
### Assessment 

### Determine Azure SQL platform

This [article](https://learn.microsoft.com/en-us/azure/azure-sql/azure-sql-iaas-vs-paas-what-is-overview?view=azuresql&viewFallbackFrom=sql-server-ver16) exaplains the capabilities of Azure SQL and the different options available. 

This [article](https://learn.microsoft.com/en-us/dotnet/azure/migration/sql) provides and overview of the Azure SQL options for migration.  

This is a training [resource](https://learn.microsoft.com/en-us/training/modules/deploy-paas-solutions-with-azure-sql/) to help with evauating and understanding the Azure SQL PaaS solutions. 

This is a landing [page](https://learn.microsoft.com/en-us/data-migration/) for data migration scenario's.  

If the outcome of the assessment is to deploy to a SQL Server on an Azure SQL Database, this [resource](https://learn.microsoft.com/en-us/azure/azure-sql/migration-guides/database/sql-server-to-sql-database-overview?view=azuresql) provides comprehensive information on the migration process.  

If the outcome of the assessment is to deploy to a SQL Server on an Azure SQL Managed Instance, this [resource](https://learn.microsoft.com/en-us/azure/azure-sql/migration-guides/managed-instance/sql-server-to-managed-instance-overview?view=azuresql) provides comprehensive information on the migration process.  

If the outcome of the assessment is to deploy to a SQL Server on an Azure Virtual Machine, this [resource](https://learn.microsoft.com/en-us/azure/azure-sql/migration-guides/virtual-machines/sql-server-to-sql-on-azure-vm-individual-databases-guide?view=azuresql) provides comprehensive information on the deployment and configuration of an Azure SQL Server Virtual Machine. 

## Migration 

### Azure Migrate

### Azure Data Studio

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

Network isolation 

Security Baseline (azure defender)
https://techcommunity.microsoft.com/t5/azure-sql-blog/summary-of-the-2022-security-investments-in-azure-sql-and-sql/ba-p/3701607
Microsoft Defender - Security Defender

Role based access control (RBAC)
Managed service identities
Always Encrypted 
Azure Key Vault 
Purview – Information Classification 

#### Cost Optimization
Azure cost management, Azure advisor, scaling considerations, serverless options pause \ resume options. Azure SQL Database has serverless options. Azure SQL Managed Instance introduced the ability to start and stop an instance. 
        
#### Operational Excellence

SQL Server best practices assessment (BPA)
https://techcommunity.microsoft.com/t5/sql-server-blog/best-practices-assessment-arc-enabled-sql-server/ba-p/3715776 

Maintence windows

##### Azure Data Studio – 

VS Code

Notebooks
TSG’s 
	

##### DevOps
Azure Data studio - Database projects
Local development

VS Code 

Microsoft SQL Server Data-Tier Application Framework DacFx
SqlPackage

Infrastructure as code

#### Performance Efficiency
Azure Portal
Azure Monitor

Query Store
Intelligent Query Processing (IQP)  
Columnstore
Non Clustered Columnstore (NCCS)
Database compatibility level 
automatic tuning 

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
