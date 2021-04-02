---
layout: page
title: SQL Server Migration to Azure
permalink: /azure/data-analytics-ai/sql-server-migration-to-azure
tags: 
 - azure
 - sql server
 - migration
---

# Learning Plan Resources for SQL Server Migration to Azure

This learning plan aggregates content for understanding and successfully migrating databases into Microsoft Azure. Specifically, this plan covers the migration of relational databases, primarily SQL Server, MySQL, Postgres, and MariaDB, with a specific emphasis on SQL Server because of the number of deployment options available.

In any database migration, it is important to have the source system documented in order to evaluate target options. For the source system, a minimum amount of information needed includes:

* Overall system size (CPU/RAM/IO subsystem), current usage, and version
* Architectural diagram showing database layout and interconnectivity.  This includes cross database connectivity, ETL processes, and any feature usage such as transactional replication.
* Security requirements: information on account types (for example, Azure AD), encryption requirements (such as TDE)
* BCDR requirements: clustering, high availability, georeplication, etc. - having defined RPO (recovery point objective) and RTO (recovery time objective) numbers are essential.

With this information, options can be evaluated for both cost and technical feasibility. For example, a large server with many interconnected databases will likely be a better fit for Azure SQL Database Managed Instance, whereas a server with dozens or hundreds of independent databases will likely be a better fit for Azure SQL Database (singleton) with Elastic Pools.

Content is broken down as follows:

* Fundamentals, Associate, Expert, Specialist: content categorized in increasing level of complexity
* Certifications: relevant Microsoft exams or certifications
* Community resources: user groups, events, blogs

## Fundamentals

_The single best resource is the Microsoft Online Migration Guide, as it allows you to select both source and target systems and see prescriptive guidance:_

* [Microsoft Online Migration Guide](https://datamigration.microsoft.com/)

### SQL Server Resources (fundamentals)

* [Data Migraton Assistant](https://docs.microsoft.com/en-us/sql/dma/dma-overview) (Microsoft Docs / Application)
  * Primary tool for evaluating a SQL Database for compatibility issues
* [Choose the Right Deployment Option in Azure SQL](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-paas-vs-sql-server-iaas) (Microsoft Docs)
  * Outlines the deployment options for SQL Server in Azure
* [SQL Server on Azure VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-overview) (Microsoft Docs)
  * Overview of best practices in creating SQL Server in VMs
* [PaaS vs IaaS - Navigating the Decision Tree](https://channel9.msdn.com/Series/SAIIK-SQL-Server-on-Azure-IaaS-Implementation-Kit/SAIIK-PaaS-vs-IaaS) (Video)
  * Presentation that contrasts Azure SQL DB and SQL in VMs.
  * Information is dated as it does not include Azure SQL Database Managed Instance, but conceptually many of the ideas apply
 
### MySQL, PostgreSQL, and MariaDB Migration Guides

* [Migrate MySQL to Azure Database for MySQL](https://datamigration.microsoft.com/scenario/mysql-to-azuremysql?step=1)
* [Migrate PostgreSQL to Azure Database for PostgreSQL](https://datamigration.microsoft.com/scenario/postgresql-to-azurepostgresql?step=1)
* [Migrate MariaDB to Azure Database for MariaDB](https://datamigration.microsoft.com/scenario/mariadb-to-azuremariadb?step=1)

## Associate

* [Data Access Migration Toolkit](https://marketplace.visualstudio.com/items?itemName=ms-databasemigration.data-access-migration-toolkit) (Tooling)
  * This cool can be useful in scanning documents/code for data access patterns.

### SQL Server Resources

* [Performance Guidelines for SQL Server on Azure VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance) (Microsoft Docs)
* [Storage Configuration for SQL Server VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-storage-configuration) (Microsoft Docs)
* [Key Causes of Performance Differences with SQL Managed Instance](https://azure.microsoft.com/blog/key-causes-of-performance-differences-between-sql-managed-instance-and-sql-server/) (Blog)
* [Microsoft Learning Path for Migrating SQL Workloads to Azure](https://docs.microsoft.com/en-us/learn/paths/migrate-sql-workloads-azure/)
  * [SQL Server Discovery using the Microsoft Assessment and Planning (MAP) toolkit](https://docs.microsoft.com/en-us/learn/modules/sql-server-discovery-using-map/)
  * [Assess and convert SQL Server Databases using the Data Migration Assistant (DMA)](https://docs.microsoft.com/en-us/learn/modules/assess-convert-sql-server-databases-using-dma/)
  * [Test and optimize SQL Server databases using the Database Experimentation Assistant (DEA)](https://docs.microsoft.com/en-us/learn/modules/test-optimize-sql-server-databases-using-dea/)
  * [Migrate SQL workloads to Azure virtual machines](https://docs.microsoft.com/en-us/learn/modules/migrate-sql-workloads-azure-virtual-machines/)
  * [Migrate SQL Workloads to Azure SQL Databases](https://docs.microsoft.com/en-us/learn/modules/migrate-sql-workloads-azure-sql-databases/)
  * [Migrate SQL Workloads to Azure Managed Instances](https://docs.microsoft.com/en-us/learn/modules/migrate-sql-workloads-azure-managed-instances/)
 * [SQL Managed Instance Network Requirements](https://docs.microsoft.com/en-us/azure/azure-sql/managed-instance/connectivity-architecture-overview#network-requirements)
 * [SQL Managed Instance Connectivity Architecture](https://docs.microsoft.com/en-us/azure/azure-sql/managed-instance/connectivity-architecture-overview)

### Pluralsight Courses

* [Pluralsight: Migrating to SQL Server 2016](https://www.pluralsight.com/courses/sqlserver-2016-upgrading-migrating)
* [Pluralsight: Azure SQL Database](https://www.pluralsight.com/courses/azure-sql-database-dba)

### Youtube Video Series

* [Azure SQL Bootcamp](https://www.youtube.com/watch?v=wntLOJRvIeI&list=PLlrxD0HtieHjveswk8_gkPD42Te48X4zG)


## Expert

* [Migrate SQL Server to Azure SQL DB](https://docs.microsoft.com/en-us/azure/dms/tutorial-sql-server-to-azure-sql) (Tutorial)

## Certifications

* [AZ-900 Microsoft Certification](https://docs.microsoft.com/en-us/learn/certifications/exams/az-900)
* [DP-300: Administering Relational Databases on Microsoft Azure](https://docs.microsoft.com/en-us/learn/certifications/exams/dp-300) 
