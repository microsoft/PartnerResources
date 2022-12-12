---
layout: page
title: Microsoft Sentinel
description: Resources for Microsoft Sentinel
updated: 2022-12-12
permalink: /modern-workplace/security/microsoft-sentinel
tags:
- learning plan
- security
- microsoft security academy
- siem & xdr
- sentinel resources
---

# Microsoft Sentinel Readiness Resources
Below you will find content to assist in upskilling on Microsoft Sentinel. Content is organized by increasing levels of complexity (Fundamentals, Associate) followed by other associated critical resources.

## Fundamentals
* [Microsoft Sentinel Documentation - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/)
* [Microsoft Sentinel Technical Playbook for MSSPs](http://aka.ms/azsentinelmssp)
     * Insights on how MSSPs can configure and add value to Microsoft Sentinel
* [Microsoft Sentinel Pricing](https://azure.microsoft.com/en-us/pricing/details/azure-sentinel/)
* [Microsoft Sentinel Wiki](https://github.com/Azure/Azure-Sentinel/wiki)
* [Design your Microsoft Sentinel Workspace Architecture - Microsoft Learn](https://learn.microsoft.com/en-us/azure/sentinel/design-your-workspace-architecture#decision-tree)

#### Building a Demo. Instance
Use these steps to build a demo instance; free for one month

1. [Microsoft Sentinel Training Lab](https://github.com/Azure/Azure-Sentinel/tree/master/Solutions/Training/Azure-Sentinel-Training-Lab)
   * Initial Setup ("Dummy Data")
2. [Deploy & Monitor Azure Key Vault Honeytokens with Microsoft Sentinel - Microsofts Docs](https://docs.microsoft.com/en-us/azure/sentinel/monitor-key-vault-honeytokens?tabs=deploy-at-scale)
   * *Optional*
3. [Connect AWS Accounts to Microsoft Defender for Cloud - Microsofts Docs](https://docs.microsoft.com/en-us/azure/defender-for-cloud/quickstart-onboard-aws?pivots=env-settings)
   * *Optional*
4. [Connect Microsoft Defender for Cloud Alerts to Microsoft Sentinel - Microsofts Docs](https://docs.microsoft.com/en-us/azure/sentinel/connect-defender-for-cloud)
   * Microsoft Defender for Cloud Connector
5. [Alert Validation in Microsoft Defender for Cloud - Microsoft Docs](https://docs.microsoft.com/en-us/azure/defender-for-cloud/alert-validation)
   * Used for Sample Security Alerts
6. [Send Logs to Azure Monitor - Microsoft Docs](https://learn.microsoft.com/en-us/azure/active-directory/reports-monitoring/howto-integrate-activity-logs-with-log-analytics#send-logs-to-azure-monitor)
7. [Connect Azure Active Directory (Azure AD) Data to Microsoft Sentinel - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/connect-azure-active-directory)
8. [Connect Microsoft Sentinel to AWS to Ingest AWS Service Log Data - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/connect-aws?tabs=ct)
9. [Possible Additional Data](https://github.com/OTRF/Microsoft-Sentinel2Go)
   * Microsoft Sentinel To-Go is an open source project developed to expedite the deployment of a Microsoft Sentinel lab along with other resources for research purposes. (i.e., more "Dummy Data")

## Associate
* [Microsoft Sentinel Workspace Architecture Best Practices  - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/best-practices-workspace-architecture)
* [Microsoft Sentinel Sample Workspace Designs - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/sample-workspace-designs)
* [Microsoft 365 Defender Integration with Microsoft Sentinel - Microsoft Docs](https://learn.microsoft.com/en-us/microsoft-365/security/defender/microsoft-365-defender-integration-with-azure-sentinel?view=o365-worldwide)
* [Find your Microsoft Sentinel Data Connector - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/data-connectors-reference)
* [Resources for Creating Microsoft Sentinel Custom Connectors - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/create-custom-connector#compare-custom-connector-methods)
* [Ingest, Archive, Search, and Restore Data in Microsoft Sentinel - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/ingest-archive-search-and-restore-data-in-microsoft-sentinel/ba-p/3195126)
* [Enrich Incidents using Entity Mapping - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/entities#entity-mapping)
* [Behind the Scenes: The ML Approach for Detecting Advanced Multistage Attacks with Sentinel Fusion - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/behind-the-scenes-the-ml-approach-for-detecting-advanced/ba-p/3239236)


#### Build an SOC & Operationalize Security Operations
* [What's New: Azure Sentinel - SOC Process Framework Workbook - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/what-s-new-azure-sentinel-soc-process-framework-workbook/ba-p/2339315)
* [SOC Process Framework Overview - YouTube](https://www.youtube.com/watch?v=RnPMwy7AoS0&amp;list=PL3sJcHWKYIVPhCDIdZjVueLIkAfXijylG)

#### Agents Resources
* [Overview of the Azure Connected Machine Agent (Azure Arc) - Microsoft Docs](https://learn.microsoft.com/en-us/azure/azure-arc/servers/agent-overview)
* [Connect Hybrid Machines to Azure at Scale (Azure Arc) -  Microsoft Docs](https://learn.microsoft.com/en-us/azure/azure-arc/servers/onboard-service-principal)
* [Azure Monitor Agent Overview - Microsoft Docs](https://learn.microsoft.com/en-us/azure/azure-monitor/agents/agents-overview)

#### KQL
* [KQL for Microsoft Sentinel Lab & Queries](https://github.com/reprise99/Sentinel-Queries)
* [MustLearnKQL Blog Series](https://github.com/rod-trent/MustLearnKQL)
* [KQL Cheat Sheet](https://www.mbsecure.nl/blog/2019/12/kql-cheat-sheet)
* [Advanced KQL Framework Workbook - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/advanced-kql-framework-workbook-empowering-you-to-become-kql/ba-p/3033766)

#### ADX
   * [What is a free Azure Data Explorer Cluster? - Microsoft Docs](https://docs.microsoft.com/en-us/azure/data-explorer/start-for-free)
      * Free cluster, only a Microsoft Identity is required
   * [Azure Data Explorer in 60 minutes with Samples - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/azure-data-explorer-blog/azure-data-explorer-in-60-minutes-with-the-new-samples-gallery/ba-p/3447552)

#### Notebooks
* [Becoming a Microsoft Sentinel Notebooks Ninja - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/becoming-a-microsoft-sentinel-notebooks-ninja-the-series/ba-p/2693491)
* [Getting Started with Sentinel Notebooks - YouTube](https://www.youtube.com/watch?v=TgRRJeoyAYw)
* [Azure Sentinel Notebooks Lab](https://github.com/Azure/Azure-Sentinel-Notebooks/tree/7402ad1fc35fc78c05c51fe068ea547f928000af)

#### Migration
* [Plan Migration to Microsoft Sentinel - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/migration)
* [Microsoft Sentinel Migration: Select Target Azure Platform for Exported Data - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/migration-ingestion-target-platform)
* [Microsoft Sentinel Migration: Select Data Ingestion Tool - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/migration-ingestion-tool)
* [Best Practices for Migrating Detection Rules from ArcSight, Splunk and QRadar - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/best-practices-for-migrating-detection-rules-from-arcsight/ba-p/2216417)
* [Microsoft Sentinel Repository](https://github.com/Azure/Azure-Sentinel)
* [Unicoder Sigma Rule Converter for SIEM, EDR, & NTDR](https://uncoder.io/)
* [Azure Sentinel Side-by-Side with QRader](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/azure-sentinel-side-by-side-with-qradar/ba-p/1488333)
* [Azure Sentinel Side-by-Side with Splunk](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/azure-sentinel-side-by-side-with-splunk/ba-p/1211266)

#### Build Solutions & Other Contributions
* [Guide to Building Microsoft Sentinel Solutions](https://github.com/Azure/Azure-Sentinel/tree/master/Solutions#guide-to-building-microsoft-sentinel-solutions)

#### Risk IQ Integration
* [RiskIQ Illuminate Content Hub Solution within Microsoft Sentinel – My Faber Security](https://myfabersecurity.com/2022/03/04/riskiq-illuminate-content-hub-solution-within-microsoft-sentinel/)

#### Repositories
* [Enable Continuous Deployment Natively with Microsoft Sentinel Repositories - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/enable-continuous-deployment-natively-with-microsoft-sentinel/ba-p/2929413)
* [Microsoft Sentinel As-A-Code Lab](https://github.com/sreedharande/Microsoft-Sentinel-As-A-Code)

#### Storage options
* [Refer to Microsoft Sentinel Technical Playbook for MSSPs](http://aka.ms/azsentinelmssp)

#### Costs
* [Microsoft Sentinel Pricing](https://azure.microsoft.com/en-us/pricing/details/microsoft-sentinel/)
* [Microsoft Sentinel Cost Calculator](https://cloudpartners.transform.microsoft.com/download?assetname=assets/Azure_Sentinel_Calculator.xlsx&download=1)
* [Azure Data Explorer (Kusto) Cost Estimator](https://dataexplorer.azure.com/AzureDataExplorerCostEstimator.html)

#### Data at No-Cost
Microsoft Sentinel and Log Analytics offer ingestion & 90-day retention of *some* data at no cost, including:
   * Azure Activity Logs
   * Office 365 Audit Logs (e.g., SharePoint, Exchange, Teams)
   * Alerts from Microsoft Defender products
   * Microsoft Defender for IoT

Reference [Plan Costs and Microsoft Sentinel Pricing and Billing - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/billing?tabs=commitment-tier) for further information.

#### Other Ways to Save
* [Microsoft Sentinel Benefit for Microsoft 365 E5, A5, F5, and G5 Customers](https://azure.microsoft.com/en-us/offers/sentinel-microsoft-365-offer/#:~:text=Microsoft%20Sentinel%20benefit%20for%20Microsoft%20365%20E5%2C%20A5%2C,scale.%204%20Enable%20efficient%20and%20effective%20response%20) 
* [Locate Microsoft Sentinel Free Benefit in Cost Management & Billing](https://azurecloudai.blog/2022/03/15/how-to-locate-the-microsoft-sentinel-free-benefit-in-cost-management-billing/)
* Commitment Tiers; save up to 65% compared to pay-as-you-go.
