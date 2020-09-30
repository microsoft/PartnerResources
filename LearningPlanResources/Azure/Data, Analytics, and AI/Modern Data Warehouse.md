# Learning Plan Resources for Modern Data Warehouse

Azure Synapse is an analytical service evolved from Azure SQL Data Warehouse that brings together enterprise data warehousing and big data analytics.  Provisioned or on-demand, Azure Synapse offers a unified experience to ingest, prepare, manage, and serve data for analytics, BI, and machine learning needs.

Below you will find content to assist in upskilling in Azure Synapse.  Because the product is rapidly evolving, some documentation may reference Azure SQL Data Warehouse, or refer to features that are in-preview and not yet released.  Content is broken down as follows:
* Fundamentals, Associate, Expert, Specialist: content categorized in increasing level of complexity
* Certifications: relevant Microsoft exams or certifications
* Community resources: user groups, events, blogs

Additionally, some content may be marked with one or more icons:
* '$' to indicate paid content
* '3rd Party' to indicate 3rd party content (not created by Microsoft)

## Fundamentals

* [Introducing Azure Synapse Analytics](https://myignite.techcommunity.microsoft.com/sessions/81578?source=sessions
 ) (Ignite session / 1 hour)
    * Customer talk track on the problems that Azure Synapse is designed to address. 
* [Data Warehouse workloads](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/big-data) (Microsoft Docs)
    * Defines the building blocks and workloads for a Modern Data Warehouse.
    * Big Data is a synonym for Modern Data Warehouse in this article
* [Azure Data Architecture Guide](https://docs.microsoft.com/en-us/azure/architecture/data-guide/) (Microsoft Docs) 
    * Azure Data architecture guide is a deep dive into each workload in a Modern Data Warehouse
    * Review all content under the "Guides" directory on the left-hand menu
* [Data Management Patterns](https://docs.microsoft.com/en-us/azure/architecture/patterns/category/data-management) (Microsoft Docs) 
    * These are different design patterns your Data Warehouse might need to address
    * Database Developers or Administrator might use these terms to define their current architecture
* [What is Data Engineering?](https://medium.com/datadriveninvestor/what-is-data-engineering-explaining-the-data-pipeline-data-warehouse-and-data-engineer-role-1a4b182e0d16) (3rd Party, Document)
    * Industry definition of a data warehouse, ETL and data engineer
    * Provide a common set of concept and terms you need to know when talking with your customers
* [Understanding Star Schema](https://docs.microsoft.com/en-us/power-bi/guidance/star-schema) (Microsoft Docs)
    * How best to model your business data for analytics
    * Star schemas are defined as dimensional models and central to data warehouse analysis
* [AWS to Azure Services Comparison](https://docs.microsoft.com/en-us/azure/architecture/aws-professional/services
) (Microsoft Docs)
    * Reference guide for alternative Cloud platforms
* [Azure Partner Tech Talks - Modern Data Warehouse](http://aka.ms/azurepartnerstechtalks) (Webinar)
     * Specifically, the Modern Data Warehouse presentation from April 23, 2020

## Associate

* [Introducing the Modern Data Warehouse Solution Pattern](https://youtube.com/watch?v=7MDCWgxPnVY) (YouTube, ~20 minutes)
* [Big Data Architectures](https://docs.microsoft.com/en-us/azure/architecture/data-guide/big-data/) (Microsoft Docs)
    * Review all content under "Big Data" directory on left-hand menu
* [Modern Data Warehouse Architecture](https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/articles/modern-data-warehouse) (Microsoft Docs)
    * Reference architecture for a Modern Data Warehouse
* [Implement a Data Warehouse with Azure Synapse Analytics](https://docs.microsoft.com/en-us/learn/paths/implement-sql-data-warehouse/) (Microsoft Docs)
    * Hands-on lab with three modules to complete.
* [Azure SQL Database vs SQL Data Warehouse](https://www.jamesserra.com/archive/2016/08/azure-sql-database-vs-sql-data-warehouse/) (Microsoft Blog)
    * Decision criteria for best Azure Data Service for data warehousing
* [Dimensional Modelling Case Study: eWallet](https://towardsdatascience.com/data-warehouse-dimensional-modelling-use-case-study-ewallet-d9d16f559181) (3rd Party, Document)
* [Power BI Guidance](https://docs.microsoft.com/en-us/power-bi/guidance/) (Microsoft Docs)
    * Review all content in the Data Modeling section.
* [Criteria for Choosing a Data Store](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/data-store-comparison) (Microsoft Docs)
    * Alternative options to relational databases.
* [Azure Data Factory: Mapping Data Flows](https://github.com/kromerm/adfdataflowdocs/blob/master/patterns/adfdataflowlinks.md) (Tutorials) 
    * Review all content and complete NYC Taxi Demo Lab
* [Extending on-premises data solutions to the cloud](https://docs.microsoft.com/en-us/azure/architecture/data-guide/scenarios/hybrid-on-premises-and-cloud) (Microsoft Docs)
    * Azure Services required for a Hybrid architecture
* [Securing Data Solutions](https://docs.microsoft.com/en-us/azure/architecture/data-guide/scenarios/securing-data-solutions) (Microsoft Docs)
    * General security requirements needed for any data platform architecture
* [Architect Migration and BCDR](https://docs.microsoft.com/en-us/learn/paths/architect-migration-bcdr/) (Microsoft Docs)

_The following documents are intended to be consumed in order, as they begin with a reference architecture through solution building:_

* [1. Reference Architecture: Automated Enterprise BI with Synapse](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/data/enterprise-bi-adf) (Microsoft Docs)
* [2. Example Workloads: Data warehousing and analytics](https://docs.microsoft.com/en-us/azure/architecture/example-scenario/data/data-warehouse) (Microsoft Docs)
* [3. Solution Ideas: Streaming using HDInsight](https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/articles/streaming-using-hdinsight) (Microsoft Docs)

_Pluralsight Courses:_

* [Implementing a Cloud Data Warehouse in Microsoft Azure Synapse Analytics](https://www.pluralsight.com/courses/microsoft-azure-implementing-cloud-data-warehouses) (3rd Party, $)
* [Modern Data Warehousing at Scale Using Azure Data Factory](https://www.pluralsight.com/courses/big-data-ldn-session-25) (3rd Party)
    * This is a session from Big Data LDN in Nov 2019. This is a good primer/use case on Azure Data Factory for ETL.

## Expert

* [Tutorial: Load data using Azure portal and SSMS](https://docs.microsoft.com/en-us/azure/synapse-analytics/sql-data-warehouse/load-data-wideworldimportersdw) (Microsoft Docs)
* [Tutorial: Load the NY Taxicab Dataset](https://docs.microsoft.com/en-us/azure/synapse-analytics/sql-data-warehouse/load-data-from-azure-blob-storage-using-polybase) (Hands on lab)
* [Building OSS Analytical Solutions with Azure HDInsight](https://docs.microsoft.com/en-us/learn/paths/build-oss-analytical-solutions-az-hdinsight/) (Microsoft Docs)
* [Azure End2End - Azure Data Platform Workshop](https://github.com/fabragaMS/ADPE2E) (Hands on lab)
* [Azure Data Factory - Labs](https://github.com/kromerm/ADF_Labs) (Hands on lab)

_WhatTheHack events are often in-person in a hands on format.  However, it can be worked on individually and self-paced:_

* [WhatTheHack - Driving Miss Data](https://github.com/microsoft/WhatTheHack/tree/master/003-DrivingMissData) (Hands on lab)

_Microsoft OpenHack events are immersive, multi-day hands on experiences; specifically, the Modern Data Warehouse dives into Azure Synapse, Databricks, Azure Data Factory, and Azure Data Lake._
* [OpenHack - Modern Data Warehouse](https://openhack.microsoft.com/) (Hands on lab / workshop)

## Specialist

* [Open Hack Registration Site](https://openhacks.azurewebsites.net/labs/player/openhack_-_modern_data_warehousing_2bd410cacc6b_3_0)
    * Register for a Modern Data Warehouse OpenHack. OpenHacks are a challenge-based lab format; the Modern Data Warehousing OpenHack provides a lab environment with preconfigured resources.
* [Analytics in a Day](https://github.com/abrahams1/azsynapselabsny)
    * Self-guided labs for Analytics in Day workshop.

## Certifications

Exams such as the [70-767 Implementing a Data Warehouse](https://www.microsoft.com/en-us/learning/exam-70-767.aspx) are still available, however we recommend the new role-based certifications as these better align to industry trends and the mix of technical skills needed to successfully build Data & AI solutions.

Although DP-200 and DP-201 are similar, DP-200 focuses more on the "How?" solutions are implemented, typically requiring code/scripting experience and knowledge of how to enable certain features.  DP-201 focuses more on the "Why?" -- understanding how different components work together.

* [Exam DP-200: Implementing an Azure Data Solution](https://docs.microsoft.com/en-us/learn/certifications/exams/dp-200)
* [Exam DP-201: Designing an Azure Data Solution](https://docs.microsoft.com/en-us/learn/certifications/exams/dp-201)

Both of these exams are required for the [Microsoft Certified: Azure Data Engineer Associate](https://docs.microsoft.com/en-us/learn/certifications/azure-data-engineer?wt.mc_id=learningredirect_certs-web-wwl) certification.

## Community

* [Power BI User Group](https://www.pbiusergroup.com/home)
* [SQL PASS](https://www.pass.org/)
* [Pragmatic Works: Blog on SQL Server](https://blog.pragmaticworks.com)
* [Blue Granite Blog](https://www.blue-granite.com/blog)
* [Buck Woody's Blog](https://buckwoody.wordpress.com/)
* [James Serra's Blog](https://www.jamesserra.com/)


Your added/modified content
