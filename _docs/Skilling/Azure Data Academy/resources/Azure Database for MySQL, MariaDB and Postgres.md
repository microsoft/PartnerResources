---
layout: page
title: OSS DB to Azure
description: Resources for Azure Database for MySQL, MariaDB, and Postgres
updated: 2022-09-30
permalink: /skilling/azure-data-academy/resources/oss-db-to-azure
tags: 
- azure
- data, analytics, and ai
- learning plan
- resources
- postgres
- mysql
- database
- azure data academy
---

# Azure Database for MySQL, MariaDB, and Postgres Readiness Resources

This learning plan aggregates content for understanding and successfully migrating databases into Microsoft Azure. Migration implies there is a "from" source and a "to" destination. This plan covers a base understanding of, and the migration of relational databases TO, the various open source relational database services in Azure:
- Azure Database for MySQL
- Azure Database for MariaDB
- Azure Database for PostgreSQL

In any database migration, it is important to have the source system documented in order to evaluate target options. For the source system, a minimum amount of information needed includes:

- Overall system size (CPU/RAM/IO subsystem), current usage, and version
- Architectural diagram showing database layout and interconnectivity. This includes cross database connectivity, ETL processes, and any feature usage such as transactional replication.
- Security requirements: information on account types (for example, Azure AD), encryption requirements (such as TDE)
- BCDR requirements: clustering, high availability, georeplication, etc. - having defined RPO (recovery point objective) and RTO (recovery time objective) numbers are essential.

With this information, options can be evaluated for both cost and technical feasibility. 

Content is broken down as follows:

Fundamentals, Associate, Expert, Specialist: content categorized in increasing level of complexity
Certifications: relevant Microsoft exams or certifications
Community resources: user groups, events, blogs

## Fundamentals

We all have to start somewhere. Start by learning about the various relational database offerings on Azure.  This includes Azure SQL Database as well as the open source database offerings too. Then get an overview of each individual open source database service on Azure.
- [Microsoft Azure Data Fundamentals: Explore relational data in Azure](https://learn.microsoft.com/en-us/training/paths/azure-data-fundamentals-explore-relational-data/) (Learning Path - 73 mins)
- [Introduction to Azure Database for PostgreSQL](https://docs.microsoft.com/en-us/learn/modules/intro-to-postgres/) (Self-Paced) (20 minute read)
- [Create and connect to an Azure Database for PostgreSQL](https://docs.microsoft.com/en-us/learn/modules/create-connect-to-postgres/) (Self-Paced) (46 minutes)
- [Introduction to Azure Database for MySQL](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-database-for-mysql/) (40 minute read)
- [Introduction to Azure Database for MariaDB](https://learn.microsoft.com/en-us/training/modules/intro-to-azure-database-for-mariadb/) (35 minute read)

Know where to find the documentation for each of these offerings:

- [Azure Database for PostgreSQL Documentation](https://learn.microsoft.com/en-us/azure/postgresql/)
- [Azure Database for MySQL Documentation](https://learn.microsoft.com/en-us/azure/mysql/)
- [Azure Database for MariaDB Documentation](https://learn.microsoft.com/en-us/azure/mariadb/)

For MySQL and PostgreSQL, understand the differences between "single server" and "flexible server":

MySQL options:
- [Azure Database for MySQL - Single Server](https://learn.microsoft.com/en-us/azure/mysql/single-server/single-server-overview)
- [Azure Database for MySQL - Flexible Server](https://learn.microsoft.com/en-us/azure/mysql/flexible-server/overview)
**NOTE:** MySQL Single Server is being retired. Read here for details: [What's happening to Azure Database for MySQL - Single Server?](https://learn.microsoft.com/en-us/azure/mysql/single-server/whats-happening-to-mysql-single-server)
- [Choose the right MySQL Server option in Azure](https://learn.microsoft.com/en-us/azure/mysql/single-server/select-right-deployment-type)

PostgreSQL options:
- [Azure Database for PostgreSQL - Single Server](https://learn.microsoft.com/en-us/azure/postgresql/single-server/overview-single-server)
- [Azure Database for PostgreSQL - Flexible Server](https://learn.microsoft.com/en-us/azure/postgresql/flexible-server/overview)
- [Comparison chart - Azure Database for PostgreSQL Single Server and Flexible Server](https://learn.microsoft.com/en-us/azure/postgresql/flexible-server/concepts-compare-single-server-flexible-server)

For PostgreSQL, there is a new option called Azure CosmosDB for PostgreSQL.  This was formerly known as "Azure Database for PostgreSQL Hyperscale":
- [Azure CosmosDB for PostgreSQL](https://learn.microsoft.com/en-us/azure/cosmos-db/postgresql/introduction)
- [Distributed PostegreSQL comes to Azure CosmosDB](https://devblogs.microsoft.com/cosmosdb/distributed-postgresql-comes-to-azure-cosmos-db/)

### Migration Options

Once you understand the open source database service options in Azure, you should start to review options for migrating TO them FROM various sources. Start with the "Azure Database Migration Guides" listing which aggregates many of the individual migration guides below in one place.

- [Azure Database Migration Guides](https://learn.microsoft.com/en-us/data-migration) 
  - [Migrate MySQL on-premises to Azure Database for MySQL](https://learn.microsoft.com/en-us/azure/mysql/migrate/mysql-on-premises-azure-db/01-mysql-migration-guide-intro)
  - [Migrate your MySQL database by using import and export](https://learn.microsoft.com/en-us/azure/mysql/single-server/concepts-migrate-import-export)
  - [Migrate your MariaDB database to an Azure Database for MariaDB by using dump and restore](https://learn.microsoft.com/en-us/azure/mariadb/howto-migrate-dump-restore)
  - [Migrate your PostgreSQL database by using dump and restore](https://learn.microsoft.com/en-us/azure/postgresql/migrate/how-to-migrate-using-dump-and-restore)
  - [Migrate Oracle to Azure Database for PostgreSQL](https://learn.microsoft.com/en-us/azure/postgresql/migrate/how-to-migrate-from-oracle)


* [MySQL Server - Replicate Changes in Azure Database Migration Service](https://techcommunity.microsoft.com/t5/microsoft-data-migration-blog/azure-dms-mysql-replicate-changes-now-in-preview/ba-p/3601564)
  * New functionality to support migration by replicating changes while databases continue to be operational.

### Azure Data Academy series

Like sitting back and watching videos to learn? Check out the video series below with sessions on MySQL, PostgreSQL, and SQL Server.
- [Azure Data Academy series](https://aka.ms/ada)

## Associate

If you've made it through the fundamentals above, you might want to dig into some of the migration tools and topics here.

- [Microsoft Learn - Azure Database for PostgreSQL - Beginner and Intermediate modules](https://learn.microsoft.com/en-us/training/browse/?products=azure-database-postgresql&filter-products=postgresql)
  - Microsoft Learn has many "Learning Path" modules that take you through various PostgreSQL concepts. This is a great resource for digging deeper into Azure Database for PostgreSQL.
- [Microsoft Learn - Azure Database for MySQL - Beginner and Intermediate modules](https://learn.microsoft.com/en-us/training/browse/?filter-products=mysql&products=azure-database-mysql)
  - Microsoft Learn has many "Learning Path" modules that take you through various MySQL concepts. This is a great resource for digging deeper into Azure Database for MySQL.
- [Ingest and query data using Azure CosmosDB for PostgreSQL](https://learn.microsoft.com/en-us/training/modules/ingest-query-data-using-azure-cosmos-db-for-postgresql/)
  - This Microsoft Learning module will help you learn the basics of Azure CosmosDB for PostgreSQL by setting one up.   
- [Limitations in Azure Database for MySQL](https://learn.microsoft.com/en-us/azure/mysql/single-server/concepts-limits)
  - Nothing is perfect in life.  There are always gotchas.  Here is a list of them to have handy for MySQL.
- [Limitations in Azure Database for PostgreSQL](https://learn.microsoft.com/en-us/azure/postgresql/single-server/concepts-limits)
  - Nothing is perfect in life.  There are always gotchas.  Here is a list of them to have handy for PostgreSQL.

### Tools
- [Azure OSS DB SKU Recommender](https://github.com/izzymsft/azureossdbskurecommender)
  - Not sure which SKU of Azure Database for PostgreSQL or MySQL you should use?  This utility is designed to connect to your existing on-prem database, analyze it, and provide you with a a set of recommendations.
- [Oracle to Azure Database for Postgres Migration Guide](https://github.com/microsoft/OrcasNinjaTeam/blob/master/Oracle%20to%20PostgreSQL%20Migration%20Guide/Oracle%20to%20Azure%20Database%20for%20PostgreSQL%20Migration%20Guide.pdf) (Self-Paced) (5 Hours)
  - If you are looking to migrate an Oracle database to Azure Database for PostgreSQL, this in-depth PDF whitepaper has you covered.  At 309 pages, it is a long read, but it is THE definitive guide on this migration path.
- [Azure Data Studio](https://learn.microsoft.com/en-us/sql/azure-data-studio/what-is-azure-data-studio?view=sql-server-ver16)
  - Azure Data Studio is a tool that any DBA working with Azure should have in their toolbox. Based on the same technology as [Visual Studio Code](https://code.visualstudio.com/), Azure Data Studio provides you an extensible tool that lets you connect to and manage many different types of databases.
  - [PostgreSQL extension for Azure Data Studio](https://learn.microsoft.com/en-us/sql/azure-data-studio/extensions/postgres-extension?view=sql-server-ver16)
  - [Database Migration Assessment for Oracle extension](https://learn.microsoft.com/en-us/sql/azure-data-studio/extensions/database-migration-assessment-for-oracle-extension?view=sql-server-ver16)
- [Ora2PG Tool](https://ora2pg.darold.net/)
  - Ora2Pg is a free tool used to migrate an Oracle database to a PostgreSQL compatible schema. It connects your Oracle database, scans it automatically and extracts its structure or data, then generates SQL scripts that you can load into your PostgreSQL database.
  - Ora2Pg can be used for anything from reverse engineering Oracle database to huge enterprise database migration or simply replicating some Oracle data into a PostgreSQL database. It is really easy to use and doesn't require any Oracle database knowledge other than providing the parameters needed to connect to the Oracle database.

### Learn How to Migrate to Azure Database for PostgreSQL or MySQL through What The Hack

[What the Hack](https://aka.ms/wth) is a set of challenge based hackathons that can be hosted in-person or virtually via Microsoft Teams.

If you are interested in attending a What The Hack event, contact your Microsoft Partner representative.  Alternatively, you can host one yourself using the guidance in the [What The Hack Hosting Guide](https://aka.ms/wthhost)

- [What The Hack: Intro to OSS DB Migration to Azure OSS DB](https://microsoft.github.io/WhatTheHack/033-OSSDatabaseMigration/) (In-person Instructor Led)

This intro level hackathon will help you get hands-on experience migrating databases from on-premises PostgreSQL, Oracle and/or MySQL to Azure DB for PostgreSQL and/or Azure DB for MySQL.

This hack features seven technical challenges that give you hands-on experience performing any (or all) of the migration permutations that you are interested in from a set of "source" databases to one of the Azure open source database options. By the end, you should have a good understanding of migration options, approaches, and tools that can help you get the job done.

## Certifications

- [AZ-900: Microsoft Azure Fundamentals](https://docs.microsoft.com/en-us/learn/certifications/exams/az-900) (Self-Paced) (4 Hours)
- [DP-900: Microsoft Azure Data Fundamentals](https://learn.microsoft.com/en-us/certifications/exams/dp-900)

## Community Resources

- [Microsoft Data Migration Blog](https://techcommunity.microsoft.com/t5/microsoft-data-migration-blog/bg-p/MicrosoftDataMigration)
  - Like all of the stuff you have read here on this Readiness Resource list?  If so, you will want to keep up to date by following the Microsoft Data Migration blog.  This blog is updated 1-2x/month by the product team and has news and announcements about features on the Azure open source database services.


