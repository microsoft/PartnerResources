---
layout: page
title: Microsoft Sentinel
description: Resources for Microsoft Sentinel
updated: 2024-09-25
permalink: /security/microsoft-security-academy/microsoft-sentinel
tags:
- security
- learning plan
- microsoft security academy
- siem & xdr
- sentinel resources
---

# Microsoft Sentinel Resources
Below, you'll find resources to help you upskill on Microsoft Sentinel. Content is arranged by increasing levels of complexity (Fundamentals, Associate) followed by other associated essential resources.


<div>&nbsp;</div>


## September 2024 Update📰

* **NEW:** [Optimize Costs using Auxiliary Logs for Verbose Logging](https://mortenknudsen.net/?p=3308&utm_source=substack&utm_medium=email) -- *Auxiliary Logs = Basic Logs + Archive Tier*
* **NEW:** [SIEM Migration Update: Now Migrate with Contextual Depth in translations with Microsoft Sentinel](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/siem-migration-update-now-migrate-with-contextual-depth-in/ba-p/4241234?utm_source=substack&utm_medium=email) -- The SIEM Migration Experience now supports Schema Mapping, Splunk Macros in translation, and Splunk Lookups in translation
* **NEW:** [Hunting with Microsoft Graph activity logs](https://techcommunity.microsoft.com/t5/microsoft-security-experts-blog/hunting-with-microsoft-graph-activity-logs/ba-p/4234632) -- Microsoft Graph is a unified REST API endpoint that  provides access to a suite of services including Microsoft 365, Enterprise Mobility + Security, and Windows
* **NEW:** [Announcing Microsoft Sentinel All-in-One v2](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/announcing-microsoft-sentinel-all-in-one-v2/ba-p/3800037) -- Microsoft Sentinel All-in-One helps customers and partners quickly deploy a ready-to-use Microsoft Sentinel environment
* [Hunting for MFA manipulations in Entra ID tenants using KQL)](https://techcommunity.microsoft.com/t5/microsoft-security-experts-blog/hunting-for-mfa-manipulations-in-entra-id-tenants-using-kql/ba-p/4154039?s=09&utm_source=substack&utm_medium=email) -- Unrelated to Sentinel, but learn how to use KQL to detect and investigate modifications to MFA properties in Microsoft Entra audit logs
* [Migrate to Microsoft Sentinel with the new SIEM Migration Experience (Preview)](https://learn.microsoft.com/en-us/azure/sentinel/siem-migration)
* [Data Connectors: MMA vs AMA](https://www.linkedin.com/pulse/cef-data-connector-mma-vs-ama-debac-manikandan-fo36c/?utm_source=share&utm_medium=member_android&utm_campaign=share_via)
* [Data Connectors: AWS vs AWS S3](https://www.linkedin.com/pulse/data-connector-aws-vs-s3-debac-manikandan-vfhcc%3FtrackingId=CUG5RbZTglInWcBaHIvgYA%253D%253D/?trackingId=CUG5RbZTglInWcBaHIvgYA%3D%3D&utm_source=substack&utm_medium=email)
* [Before and After Archive Tier](https://www.linkedin.com/pulse/before-after-archive-tier-debac-manikandan-zxwuc/?utm_source=share&utm_medium=member_android&utm_campaign=share_via)
* [Before and After Data Collection Rules (DCRs)](https://www.linkedin.com/pulse/before-after-data-collection-rules-debac-manikandan-gyw5c/?utm_source=share&utm_medium=member_android&utm_campaign=share_via)

## Fundamentals
* [Microsoft Sentinel Technical Playbook for MSSPs](http://aka.ms/azsentinelmssp)
* [Microsoft Sentinel Pricing Calculator v2](https://cloudpartners.transform.microsoft.com/download?assetname=assets%2FAzure_Sentinel_Calculator-v2.xlsx)
* [Microsoft Sentinel Pricing](https://azure.microsoft.com/en-us/pricing/details/azure-sentinel/)
* [**GitHub:** Microsoft Sentinel Repository](https://github.com/Azure/Azure-Sentinel/wiki)
* [**GitHub:** KQL for Microsoft Sentinel Lab & Queries](https://github.com/reprise99/Sentinel-Queries)
* [**GitHub:** Threat Hunting & Detecting using KQL Queries](https://github.com/cyb3rmik3/KQL-threat-hunting-queries?utm_source=substack&utm_medium=email#kql-training)

#### Building a Demo. Instance🚀
Use these steps to build a demo instance; free for one month

1. **[Microsoft Sentinel All In One](https://aka.ms/SentinelAllInOne)** -> Accelerate Microsoft Sentinel deployment and configuration with just a few clicks.
2. [**GitHub:** Microsoft Sentinel Training Lab](https://github.com/Azure/Azure-Sentinel/tree/master/Solutions/Training/Azure-Sentinel-Training-Lab)
3. [Connect Microsoft Entra to Microsoft Sentinel](https://docs.microsoft.com/en-us/azure/sentinel/connect-azure-active-directory)

#### Ninja Trainings
* [Microsoft Sentinel Ninja Training](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/become-a-microsoft-sentinel-ninja-the-complete-level-400/ba-p/1246310)
* [Microsoft Sentinel Automation Ninja Training](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/become-a-microsoft-sentinel-automation-ninja/ba-p/3563377)
* [Microsoft Defender Threat Intelligence Ninja Training](https://techcommunity.microsoft.com/t5/microsoft-defender-threat/become-a-microsoft-defender-threat-intelligence-ninja-the/ba-p/3656965)
* [Microsoft Sentinel Notebooks Ninja Training](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/becoming-a-microsoft-sentinel-notebooks-ninja-the-series/ba-p/2693491)

#### Ingestion
* [**Microsoft Sentinel Migration:** Select Target Azure Platform for Exported Data](https://learn.microsoft.com/en-us/azure/sentinel/migration-ingestion-target-platform)
* [**Microsoft Sentinel Migration:** Select Data Ingestion Tool](https://learn.microsoft.com/en-us/azure/sentinel/migration-ingestion-tool)
* **Community:** [Refactoring Data Ingestion Costs](https://craigclouditpro.wordpress.com/2023/09/19/refactoring-data-ingestion-costs/?utm_source=substack&utm_medium=email)
* [Find your Microsoft Sentinel Data Connector](https://docs.microsoft.com/en-us/azure/sentinel/data-connectors-reference)
* [Resources for creating Microsoft Sentinel Custom Connectors](https://learn.microsoft.com/en-us/azure/sentinel/create-custom-connector)

#### Retention
* [What is a free Azure Data Explorer Cluster?](https://docs.microsoft.com/en-us/azure/data-explorer/start-for-free)

Microsoft Sentinel and Log Analytics offer ingestion & 90-day retention of *some* data at no cost, including:
   * Azure Activity Logs
   * Microsoft Sentinel Health
   * Office 365 Audit Logs (e.g., SharePoint activity, Exchange activity, Teams)
   * Alerts from Microsoft Defender products (e.g., Microsoft Defender XDR, Microsoft Defender for Cloud, etc.)
   * Azure Information Protection Alerts
   * Microsoft Defender for IoT Alerts

## Associate
* [Design your Microsoft Sentinel Workspace Architecture](https://learn.microsoft.com/en-us/azure/sentinel/design-your-workspace-architecture)
* **Community:** [Quality Assurance in Microsoft Sentinel: How to ensure accurate threat detections?](https://secopslab.substack.com/p/quality-assurance-in-microsoft-sentinel?utm_source=profile&utm_medium=reader2)
* [**MSFT Blog:** Elevating Cybersecurity Intelligence with Microsoft Sentinel's New Enrichment Widgets](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/elevating-cybersecurity-intelligence-with-microsoft-sentinel-s/ba-p/3985255?utm_source=substack&utm_medium=email)

#### Azure Lighthouse
* [Delegate Access using Azure Lighthouse for a Sentinel POC](https://myfabersecurity.com/2022/07/15/delegate-access-using-azure-lighthouse-for-a-sentinel-poc/)
* [Azure Lighthouse & Microsoft Sentinel: Assigning Access to Managed Identities in Customer Tenant](https://myfabersecurity.com/2022/08/31/azure-lighthouse-and-sentinel-assigning-access-to-managed-identities-in-the-customer-tenant/)

#### Build a Security Operations Center (SOC)
* [MSSPs and Identity: Considerations for Tenant Architecture & Delegating Access to SOC analysts](https://myfabersecurity.com/2023/01/11/mssps-and-identity/)
* [Protecting MSSP Intellectual Property in Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/mssp-protect-intellectual-property)

#### KQL
* **[MustLearnKQL Blog Series](https://github.com/rod-trent/MustLearnKQL)**
* [KQL Search](https://www.kqlsearch.com)
* [SQL to KQL Cheat Sheet](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/sqlcheatsheet)

#### SOAR
* **Community:** [SOAR Capabilities in Microsoft Sentinel](https://mccybersec.github.io/microsoft%20sentinel/SOAR-Capabilities-with-Microsoft-Sentinel/?utm_source=substack&utm_medium=email)
* **[STAT](https://aka.ms/mstat)** -- The Microsoft Sentinel Triage Assistant (STAT) uses modular playbooks and a Logic App Custom Connector to simplify the process through reusable content
* [Sample Integrations with Azure OpenAI](https://myfabersecurity.com/2023/07/29/initial-assessment-connecting-the-dots-with-aoai/)

#### UEBA
* [Updated Workbook for User and Entity Behavior Analytics (UEBA)](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/unleash-the-full-potential-of-user-and-entity-behavior-analytics/ba-p/4031570)

#### MDTI
* **Community:** [Continuously import Threat Intelligence (TI) Indicators in Microsoft Sentinel](https://mccybersec.github.io/microsoft%20sentinel/threat-intelligence-upload/?utm_source=substack&utm_medium=email)

#### Notebooks
* [Get Started with Jupyter Notebooks & MSTICPy in Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/notebook-get-started)
