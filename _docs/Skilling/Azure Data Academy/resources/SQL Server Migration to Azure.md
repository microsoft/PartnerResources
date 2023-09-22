---
layout: page
title: SQL Server Migration to Azure
description: Resources for SQL Server Migration to Azure
updated: 2021-12-01
permalink: /skilling/azure-data-academy/resources/sql-server-migration-to-azure
tags: 
- azure
- data, analytics, and ai
- learning plan
- resources
- sql server
- migration
- azure data academy
---

# SQL Server Migration to Azure Readiness Resources

This learning plan aggregates content for understanding and successfully migrating SQL Server databases into Microsoft Azure. 

In any database migration, it is important to have the source system documented in order to evaluate target options. For the source system, a minimum amount of information needed includes:

* Overall system size (CPU/RAM/IO subsystem), current usage, and version
* Architectural diagram showing database layout and interconnectivity.  This includes cross database connectivity, ETL processes, and any feature usage such as transactional replication.
* Security requirements: information on account types (for example, Azure AD), encryption requirements (such as TDE)
* BCDR requirements: clustering, high availability, georeplication, etc. - having defined RPO (recovery point objective) and RTO (recovery time objective) numbers are essential.

With this information, options can be evaluated for both cost and technical feasibility. For example, a large server with many interconnected databases will likely be a better fit for Azure SQL Database Managed Instance, whereas a server with dozens or hundreds of independent databases will likely be a better fit for Azure SQL Database (singleton) with Elastic Pools.

Content is broken down as follows:

* Pre-migration, Migration, Post-migration
* Certifications: relevant Microsoft exams or certifications
* Community resources: user groups, events, blogs

## Pre-migration

_The single best resource is the Microsoft Online Migration Guide, as it allows you to select both source and target systems and see prescriptive guidance:_

* [Microsoft Online Migration Guide](https://datamigration.microsoft.com/)

### SQL Server Resources

* [Learn how to use Transact-SQL to query data in a database](https://learn.microsoft.com/en-us/training/paths/get-started-querying-with-transact-sql/)
  * Learn how to use Transact-SQL to query data in a database
* [SQL Server Discovery using the Microsoft Assessment and Planning (MAP) toolkit](https://docs.microsoft.com/en-us/learn/modules/sql-server-discovery-using-map/) (Microsoft Learn Module)
* [Data Migraton Assistant](https://docs.microsoft.com/en-us/sql/dma/dma-overview) (Microsoft Docs \ Application)
  * Primary tool for evaluating a SQL Database for compatibility issues
* [Test and optimize SQL Server databases using the Database Experimentation Assistant (DEA)](https://docs.microsoft.com/en-us/learn/modules/test-optimize-sql-server-databases-using-dea/) (Microsoft Learn Module)
* [Azure Data Studio](https://azure.microsoft.com/en-us/products/data-studio/#features) (Microsoft Docs \ Application)
* [Plan and implement data platform resources](https://learn.microsoft.com/en-us/training/paths/plan-implement-data-platform-resources/) (Microsoft Learning Path)
  * Explore options for deployment and migration
  * Calculate resource requirements and create templates
* [PaaS vs IaaS](https://learn.microsoft.com/en-us/shows/azure-sql-for-beginners/paas-vs-iaas-5-of-61) (Video)
  * Presentation that contrasts Azure SQL DB and SQL in VMs.
  * Information is dated as it does not include Azure SQL Database Managed Instance, but conceptually many of the ideas apply
* [Migrate SQL workloads to Azure](https://learn.microsoft.com/en-us/training/paths/migrate-sql-workloads-azure/) (Micorosft Learning Path)
  * Learn how to migrate SQL Server workloads to SQL Services that exist on Azure
* [Choose the Right Deployment Option in Azure SQL](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-paas-vs-sql-server-iaas) (Microsoft Docs)
  * Outlines the deployment options for SQL Server in Azure
* [SQL Server on Azure VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-overview) (Microsoft Docs)
  * Overview of best practices in creating SQL Server in VMs
* [Checklist: Best practices for SQL Server on Azure VMs](https://learn.microsoft.com/en-us/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices-checklist?view=azuresql) (Microsoft Docs)
  * This article provides a checklist of best practices and guidelines for SQL Server on Azure Virtual Machines. The article also includes links to additional learning content.  
 
## Migration

* [Data Access Migration Toolkit](https://marketplace.visualstudio.com/items?itemName=ms-databasemigration.data-access-migration-toolkit) (Tooling)
  * This tool can be useful in scanning application source documents/code for data access patterns.

### SQL Server Resources

* [Key Causes of Performance Differences with SQL Managed Instance](https://azure.microsoft.com/blog/key-causes-of-performance-differences-between-sql-managed-instance-and-sql-server/) (Blog)
 * [SQL Managed Instance Network Requirements](https://docs.microsoft.com/en-us/azure/azure-sql/managed-instance/connectivity-architecture-overview#network-requirements)
 * [SQL Managed Instance Connectivity Architecture](https://docs.microsoft.com/en-us/azure/azure-sql/managed-instance/connectivity-architecture-overview)

## Post-migration

* [Migrate SQL Server to Azure SQL DB](https://docs.microsoft.com/en-us/azure/dms/tutorial-sql-server-to-azure-sql) (Tutorial)

### SQL Server Resources
* [Monitor and optimize operational resources in Azure SQL](https://learn.microsoft.com/en-us/training/paths/monitor-optimize-operational-resources-sql-server/) (Microsoft Learning Path)
* [Optimize query performance in Azure SQL](https://learn.microsoft.com/en-us/training/paths/optimize-query-performance-sql-server/) (Microsoft Learning Path)
  * Explore performance-related Dynamic Management Objects
  * Investigate how indexes and database design affect queries


### Pluralsight Courses

* [Pluralsight: Migrating to SQL Server 2016](https://www.pluralsight.com/courses/sqlserver-2016-upgrading-migrating) (3rd Party, $)
* [Pluralsight: Azure SQL Database](https://www.pluralsight.com/courses/azure-sql-database-dba) (3rd Party, $)

### Video Series

* [Azure SQL Bootcamp on Youtube](https://www.youtube.com/watch?v=wntLOJRvIeI&list=PLlrxD0HtieHjveswk8_gkPD42Te48X4zG)
* [Channel 9 Data Exposed](https://channel9.msdn.com/Shows/Data-Exposed)


## Certifications

* [AZ-900 Azure Fundamentals Certification](https://docs.microsoft.com/en-us/learn/certifications/exams/az-900) <br>Demonstrate a fundamental knowledge of cloud concepts, along with Azure services, workloads, security, privacy, pricing, and support
* [DP-900 Azure Data Fundamentals Certification](https://learn.microsoft.com/en-us/certifications/exams/dp-900) <br>Demonstrate knowledge of core data concepts and related Microsoft Azure data services
* [DP-300: Administering Relational Databases on Microsoft Azure](https://docs.microsoft.com/en-us/learn/certifications/exams/dp-300) <br>This exam is for database administrators who manage on-premises and cloud databases built with SQL Server and SQL database services. Candidates for this exam should have knowledge of and experience with Azure SQL Edge, Azure SQL Database, Azure SQL Managed Instance, and SQL Server on Azure Virtual Machines (Windows and Linux).
