---
layout: page
title: Microsoft Sentinel
description: Resources for Microsoft Sentinel
updated: 2024-01-26
permalink: /security/microsoft-security-academy/microsoft-sentinel
tags:
- security
- learning plan
- microsoft security academy
- siem & xdr
- sentinel resources
---

# Microsoft Sentinel Resources
Below you will find content to assist in skilling on Microsoft Sentinel. Content is organized by increasing levels of complexity (Fundamentals, Associate) followed by other associated critical resources.

See our **[Microsoft Sentinel Academy](https://microsoft.github.io/PartnerResources/skilling/microsoft-security-academy/sentinel-academy)** for video sessions, demos, and other related materials created and delivered by architects across the Global Partner Solutions (GPS) security team and beyond, who are experts in their respective fields.


## Jan. 2024 Update📰
* **NEW:** [Before and After Archive Tier](https://www.linkedin.com/pulse/before-after-archive-tier-debac-manikandan-zxwuc/?utm_source=share&utm_medium=member_android&utm_campaign=share_via)
* **NEW:** [Before and After Data Collection Rules (DCRs)](https://www.linkedin.com/pulse/before-after-data-collection-rules-debac-manikandan-gyw5c/?utm_source=share&utm_medium=member_android&utm_campaign=share_via)
* **NEW:** [Updated Workbook for User and Entity Behavior Analytics (UEBA)](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/unleash-the-full-potential-of-user-and-entity-behavior-analytics/ba-p/4031570)
* [Elevating Cybersecurity Intelligence with Microsoft Sentinel's New Enrichment Widgets](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/elevating-cybersecurity-intelligence-with-microsoft-sentinel-s/ba-p/3985255?utm_source=substack&utm_medium=email)
* [Quality Assurance in Microsoft Sentinel: How to ensure accurate threat detections?](https://secopslab.substack.com/p/quality-assurance-in-microsoft-sentinel?utm_source=profile&utm_medium=reader2)
* [Refactoring Data Ingestion Costs](https://craigclouditpro.wordpress.com/2023/09/19/refactoring-data-ingestion-costs/?utm_source=substack&utm_medium=email)
* [**MSFT Blog:** New Playbooks with tasks for BEC, Ransomware, and Phishing investigations](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/automate-tasks-management-to-protect-your-organization-against/ba-p/3884516?utm_source=substack&utm_medium=email)


## Fundamentals
* [Microsoft Sentinel Ninja Training](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/become-a-microsoft-sentinel-ninja-the-complete-level-400/ba-p/1246310)
* [Microsoft Sentinel Notebooks Ninja Training](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/becoming-a-microsoft-sentinel-notebooks-ninja-the-series/ba-p/2693491)
* [Microsoft Sentinel Automation Ninja Training](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/become-a-microsoft-sentinel-automation-ninja/ba-p/3563377)
* [Microsoft Defender Threat Intelligence Ninja Training](https://techcommunity.microsoft.com/t5/microsoft-defender-threat/become-a-microsoft-defender-threat-intelligence-ninja-the/ba-p/3656965)
* [Microsoft Sentinel Technical Playbook for MSSPs](http://aka.ms/azsentinelmssp)
* [Microsoft Sentinel Pricing](https://azure.microsoft.com/en-us/pricing/details/azure-sentinel/)
* [**GitHub:** Microsoft Sentinel Repository](https://github.com/Azure/Azure-Sentinel/wiki)
* [**GitHub:** Threat Hunting & Detecting using KQL Queries](https://github.com/cyb3rmik3/KQL-threat-hunting-queries?utm_source=substack&utm_medium=email#kql-training)


#### Building a Demo. Instance
Use these steps to build a demo instance; free for one month

1. [Microsoft Sentinel All In One](https://aka.ms/SentinelAllInOne) -> Speed up Microsoft Sentinel deployment and initial configuration tasks in a few clicks.
2. [**GitHub:** Microsoft Sentinel Training Lab](https://github.com/Azure/Azure-Sentinel/tree/master/Solutions/Training/Azure-Sentinel-Training-Lab)
3. [Connect Azure Active Directory (Azure AD) Data to Microsoft Sentinel](https://docs.microsoft.com/en-us/azure/sentinel/connect-azure-active-directory)
4. [**GitHub:** Possible Additional Data](https://github.com/OTRF/Microsoft-Sentinel2Go)
   * Microsoft Sentinel To-Go is an open-source project developed to expedite the deployment of a Microsoft Sentinel lab along with resources. (i.e., more "Dummy Data")
5. [**MSFT Blog:** Ingest Sample CEF Data into Sentinel](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/ingest-sample-cef-data-into-azure-sentinel/ba-p/1064158)
   * Sample Data CEF
6. [**MSFT Blog:** New Ingestion SampleData-as-a-Service Solution](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/new-ingestion-sampledata-as-a-service-solution-for-a-great-demos/ba-p/3598500)

## Associate
* [Design your Microsoft Sentinel Workspace Architecture](https://learn.microsoft.com/en-us/azure/sentinel/design-your-workspace-architecture#decision-tree)
* [Find your Microsoft Sentinel Data Connector](https://docs.microsoft.com/en-us/azure/sentinel/data-connectors-reference)
* [Resources for Creating Microsoft Sentinel Custom Connectors](https://learn.microsoft.com/en-us/azure/sentinel/create-custom-connector#compare-custom-connector-methods)

#### Azure Lighthouse
* [Delegate Access using Azure Lighthouse for a Sentinel POC](https://myfabersecurity.com/2022/07/15/delegate-access-using-azure-lighthouse-for-a-sentinel-poc/)
* [Azure Lighthouse & Microsoft Sentinel: Assigning Access to Managed Identities in Customer Tenant](https://myfabersecurity.com/2022/08/31/azure-lighthouse-and-sentinel-assigning-access-to-managed-identities-in-the-customer-tenant/)

#### Build a Security Operations Center (SOC)
* [Protecting MSSP Intellectual Property in Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/mssp-protect-intellectual-property)
* [MSSPs and Identity: Considerations for Tenant Architecture & Delegating Access to SOC analysts](https://myfabersecurity.com/2023/01/11/mssps-and-identity/)

#### Agents Resources
* [Azure Monitor Agent Overview](https://learn.microsoft.com/en-us/azure/azure-monitor/agents/agents-overview)
* [Data Collection Rules in Azure Monitor - Microsoft Docs](https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/data-collection-rule-overview)
* [**GitHub:** Microsoft Sentinel Transformations Library](http://aka.ms/sentinel-transforms)
* [Overview of the Azure Connected Machine Agent (Azure Arc)](https://learn.microsoft.com/en-us/azure/azure-arc/servers/agent-overview)
* [**GitHub:** Azure Monitor Agent Migration (Remove Log Analytics Agent) Lab](https://github.com/Azure/Microsoft-Defender-for-Cloud/tree/main/Powershell%20scripts/Remove%20Log%20Analytics%20Agent%20At%20Scale)

#### ADX
   * [What is a free Azure Data Explorer Cluster?](https://docs.microsoft.com/en-us/azure/data-explorer/start-for-free)
      * Free cluster, only a Microsoft Identity is required
   * [**MSFT Blog:** Azure Data Explorer in 60 minutes with Samples](https://techcommunity.microsoft.com/t5/azure-data-explorer-blog/azure-data-explorer-in-60-minutes-with-the-new-samples-gallery/ba-p/3447552)

#### KQL
* [MustLearnKQL Blog Series](https://github.com/rod-trent/MustLearnKQL)
* [**GitHub:** KQL for Microsoft Sentinel Lab & Queries](https://github.com/reprise99/Sentinel-Queries)
* [KQL Cheat Sheet](https://www.mbsecure.nl/blog/2019/12/kql-cheat-sheet)
* [KQL Search](https://www.kqlsearch.com)
* [SQL to KQL Cheat Sheet](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/sqlcheatsheet)

#### Notebooks
* [Get Started with Jupyter Notebooks & MSTICPy in Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/notebook-get-started)
* [**MSFT Blog:** Hunting for Low & Slow Password Sprays Using Machine Learning](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/hunting-for-low-and-slow-password-sprays-using-machine-learning/ba-p/3592052)

#### SOAR
* **[STAT](https://aka.ms/mstat)** -- The Microsoft Sentinel Triage Assistant (STAT) uses modular playbooks and a Logic App Custom Connector to simplify the process through reusable content.
* [Sample Integrations with Azure OpenAI](https://myfabersecurity.com/2023/07/29/initial-assessment-connecting-the-dots-with-aoai/) 

#### Fusion
* [Advanced Multistage Attack Detection in Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/fusion)

#### UEBA
* [**MSFT Blog:** Microsoft Sentinel Customizable ML Based Anomalies now Generally Available](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/microsoft-sentinel-customizable-machine-learning-based-anomalies/ba-p/3624436)

#### Repositories
* [**GitHub:** Microsoft Sentinel As-A-Code Lab](https://github.com/sreedharande/Microsoft-Sentinel-As-A-Code)
* [**GitHub:** Sample Content Repository](https://github.com/SentinelCICD/RepositoriesSampleContent)

#### Migration
* [Microsoft Sentinel Migration: Select Target Azure Platform for Exported Data](https://learn.microsoft.com/en-us/azure/sentinel/migration-ingestion-target-platform)
* [Microsoft Sentinel Migration: Select Data Ingestion Tool](https://learn.microsoft.com/en-us/azure/sentinel/migration-ingestion-tool)
* [Unicoder Sigma Rule Converter for SIEM, EDR, & NTDR](https://uncoder.io/)

#### MDTI (Defender for Threat Intelligence) & Risk IQ Integration
* [**MSFT Blog:** Performing a Successful Proof of Concept (PoC)](https://techcommunity.microsoft.com/t5/microsoft-defender-threat/performing-a-successful-proof-of-concept-poc/ba-p/3742412)
* [**MSFT Blog:** Infrastructure Chaining with Microsoft Defender Threat Intelligence](https://techcommunity.microsoft.com/t5/microsoft-defender-threat/infrastructure-chaining-with-microsoft-defender-threat/ba-p/3687956)
* [RiskIQ Illuminate Content Hub Solution within Microsoft Sentinel](https://myfabersecurity.com/2022/03/04/riskiq-illuminate-content-hub-solution-within-microsoft-sentinel/)

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

Reference [Plan Costs and Microsoft Sentinel Pricing and Billing](https://learn.microsoft.com/en-us/azure/sentinel/billing?tabs=commitment-tier) for further information.