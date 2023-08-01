---
layout: page
title: Microsoft Sentinel
description: Resources for Microsoft Sentinel
updated: 2023-07-31
permalink: /security/microsoft-security-academy/microsoft-sentinel
tags:
- security
- learning plan
- microsoft security academy
- siem & xdr
- sentinel resources
---

# Microsoft Sentinel Readiness Resources
Below you will find content to assist in upskilling on Microsoft Sentinel. Content is organized by increasing levels of complexity (Fundamentals, Associate) followed by other associated critical resources.

**See our [Microsoft Sentinel Academy](https://microsoft.github.io/PartnerResources/skilling/microsoft-security-academy/sentinel-academy)** for video sessions, demonstrations and other related materials created and delivered by architects across the Global Partner Solutions (GPS) security-aligned team and beyond, who are experts in their respective fields.


## What's New
* [Automating Microsoft Sentinel Workspace Manager](https://medium.com/@TimGroothuis/diving-in-automating-sentinel-workspace-manager-cc61d536f8a6)
* [KQL Queries Behind the Microsoft Sentinel Overview Page](https://rodtrent.substack.com/p/kql-queries-behind-the-microsoft?utm_source=substack&utm_medium=email)


## Fundamentals
* [Microsoft Sentinel Ninja Training](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/become-a-microsoft-sentinel-ninja-the-complete-level-400/ba-p/1246310)
* [Microsoft Sentinel Notebooks Ninja Training](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/becoming-a-microsoft-sentinel-notebooks-ninja-the-series/ba-p/2693491)
* [Microsoft Sentinel Automation Ninja Training](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/become-a-microsoft-sentinel-automation-ninja/ba-p/3563377)
* [Microsoft Defender Threat Intelligence Ninja Training](https://techcommunity.microsoft.com/t5/microsoft-defender-threat/become-a-microsoft-defender-threat-intelligence-ninja-the/ba-p/3656965)
* [Microsoft Sentinel Technical Playbook for MSSPs](http://aka.ms/azsentinelmssp)
* [Microsoft Sentinel Pricing](https://azure.microsoft.com/en-us/pricing/details/azure-sentinel/)
* [Microsoft Sentinel Calculator](https://cloudpartners.transform.microsoft.com/download?assetname=assets%2FAzure_Sentinel_Calculator-v2.xlsx)
* [Microsoft Sentinel Repository](https://github.com/Azure/Azure-Sentinel/wiki)


#### Building a Demo. Instance
Use these steps to build a demo instance; free for one month

1. [Microsoft Sentinel Training Lab](https://github.com/Azure/Azure-Sentinel/tree/master/Solutions/Training/Azure-Sentinel-Training-Lab)
2. [Connect Azure Active Directory (Azure AD) Data to Microsoft Sentinel - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/connect-azure-active-directory)
3. [Possible Additional Data](https://github.com/OTRF/Microsoft-Sentinel2Go)
   * Microsoft Sentinel To-Go is an open source project developed to expedite the deployment of a Microsoft Sentinel lab along with other resources for research purposes. (i.e., more "Dummy Data")
4. [Ingest Sample CEF Data into Sentinel - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/ingest-sample-cef-data-into-azure-sentinel/ba-p/1064158)
   * Sample Data CEF
6. [New Ingestion SampleData-as-a-Service Solution - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/new-ingestion-sampledata-as-a-service-solution-for-a-great-demos/ba-p/3598500)

## Associate
* [Design your Microsoft Sentinel Workspace Architecture - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/design-your-workspace-architecture#decision-tree)
* [Find your Microsoft Sentinel Data Connector - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/data-connectors-reference)
* [Resources for Creating Microsoft Sentinel Custom Connectors - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/create-custom-connector#compare-custom-connector-methods)

#### Azure Lighthouse
* [Delegate Access using Azure Lighthouse for a Sentinel POC - My Faber Security](https://myfabersecurity.com/2022/07/15/delegate-access-using-azure-lighthouse-for-a-sentinel-poc/)
* [Azure Lighthouse & Microsoft Sentinel: Assigning Access to Managed Identities in Customer Tenant - My Faber Security](https://myfabersecurity.com/2022/08/31/azure-lighthouse-and-sentinel-assigning-access-to-managed-identities-in-the-customer-tenant/)

#### Build a Security Operations Center (SOC)
* [Protecting MSSP Intellectual Property in Microsoft Sentinel - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/mssp-protect-intellectual-property)
* [MSSPs and Identity - Considerations for Tenant Architecture and Delegating Access to SOC analysts](https://myfabersecurity.com/2023/01/11/mssps-and-identity/)

#### Agents Resources
* [Migrate to Azure Monitor Agent - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/azure-observability-blog/migrate-to-azure-monitor-agent-for-better-security-reliability/ba-p/3609810)
* [Azure Monitor Agent Overview - Microsoft Docs](https://learn.microsoft.com/en-us/azure/azure-monitor/agents/agents-overview)
* [Data Collection Rules in Azure Monitor - Microsoft Docs](https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/data-collection-rule-overview)
* [Overview of the Azure Connected Machine Agent (Azure Arc) - Microsoft Docs](https://learn.microsoft.com/en-us/azure/azure-arc/servers/agent-overview)
* [Azure Monitor Agent Migration (Remove Log Analytics Agent) Lab](https://github.com/Azure/Microsoft-Defender-for-Cloud/tree/main/Powershell%20scripts/Remove%20Log%20Analytics%20Agent%20At%20Scale)

#### ADX
   * [What is a free Azure Data Explorer Cluster? - Microsoft Docs](https://docs.microsoft.com/en-us/azure/data-explorer/start-for-free)
      * Free cluster, only a Microsoft Identity is required
   * [Azure Data Explorer in 60 minutes with Samples - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/azure-data-explorer-blog/azure-data-explorer-in-60-minutes-with-the-new-samples-gallery/ba-p/3447552)

#### KQL
* [MustLearnKQL Blog Series](https://github.com/rod-trent/MustLearnKQL)
* [KQL for Microsoft Sentinel Lab & Queries](https://github.com/reprise99/Sentinel-Queries)
* [KQL Cheat Sheet](https://www.mbsecure.nl/blog/2019/12/kql-cheat-sheet)
* [KQL Search](https://www.kqlsearch.com)
* [SQL to KQL Cheat sheet](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/sqlcheatsheet)

#### Notebooks
* [Get Started with Jupyter Notebooks & MSTICPy in Microsoft Sentinel - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/notebook-get-started)
* [Hunting for Low & Slow Password Sprays Using Machine Learning - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/hunting-for-low-and-slow-password-sprays-using-machine-learning/ba-p/3592052)

#### SOAR
* [Safely Integrate Playbooks with Custom APIs with no Pre-built Logic App Connector - My Faber Security](https://myfabersecurity.com/2022/11/21/safely-integrate-playbooks-with-custom-apis-when-there-is-no-pre-built-logic-app-connector/)

#### Fusion
* [Advanced Multistage Attack Detection in Microsoft Sentinel - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/fusion)

#### UEBA
* [Microsoft Sentinel Customizable Ml Based Anomalies now Generally Available - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/microsoft-sentinel-customizable-machine-learning-based-anomalies/ba-p/3624436)

#### Repositories
* [Microsoft Sentinel As-A-Code Lab](https://github.com/sreedharande/Microsoft-Sentinel-As-A-Code)
* [Sample Content Repository](https://github.com/SentinelCICD/RepositoriesSampleContent)

#### Migration
* [Microsoft Sentinel Migration: Select Target Azure Platform for Exported Data - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/migration-ingestion-target-platform)
* [Microsoft Sentinel Migration: Select Data Ingestion Tool - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/migration-ingestion-tool)
* [Unicoder Sigma Rule Converter for SIEM, EDR, & NTDR](https://uncoder.io/)

#### MDTI (Defender for Threat Intelligence) & Risk IQ Integration
* [Performing a Successful Proof of Concept (PoC)](https://techcommunity.microsoft.com/t5/microsoft-defender-threat/performing-a-successful-proof-of-concept-poc/ba-p/3742412)
* [Infrastructure Chaining with Microsoft Defender Threat Intelligence - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-defender-threat/infrastructure-chaining-with-microsoft-defender-threat/ba-p/3687956)
* [RiskIQ Illuminate Content Hub Solution within Microsoft Sentinel – My Faber Security](https://myfabersecurity.com/2022/03/04/riskiq-illuminate-content-hub-solution-within-microsoft-sentinel/)

#### Storage
* [Refer to Microsoft Sentinel Technical Playbook for MSSPs](http://aka.ms/azsentinelmssp)

#### Costs
* [Azure Data Explorer (Kusto) Cost Estimator](https://dataexplorer.azure.com/AzureDataExplorerCostEstimator.html)

#### Data at No-Cost
Microsoft Sentinel and Log Analytics offer ingestion & 90-day retention of *some* data at no cost, including:
   * Azure Activity Logs
   * Office 365 Audit Logs (e.g., SharePoint activity, Exchange activity, Teams)
   * Alerts from Microsoft Defender products
   * Azure Information Protection Alerts
   * Microsoft Defender for IoT Alerts

Reference [Plan Costs and Microsoft Sentinel Pricing and Billing - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/billing?tabs=commitment-tier) for further information.
