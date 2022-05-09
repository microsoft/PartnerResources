---
layout: page
title: Azure Sentinel
description: Resources for Azure Sentinel
updated: 2022-05-09
permalink: /modern-workplace/security/azure-sentinel
tags:
- learning plan
- azure
- modern workplace
- security
- azure sentinel
---

# Azure Sentinel Readiness Resources

Below you will find content to assist in upskilling on Azure Sentinel. Microsoft Azure Sentinel is a scalable, cloud-native, security information event management (SIEM) and security orchestration automated response (SOAR) solution. Azure Sentinel delivers intelligent security analytics and threat intelligence across the enterprise, providing a single solution for alert detection, threat visibility, proactive hunting, and threat response.

## Keeping Up
* [Azure Sentinel Technical Documentation](https://docs.microsoft.com/en-us/azure/sentinel/)
* [Security Community Webinars](https://techcommunity.microsoft.com/t5/microsoft-security-and/security-community-webinars/ba-p/927888)
* [Azure Sentinel Blog Series](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/bg-p/MicrosoftSentinelBlog)

## Fundamentals
* [MSSP Whitepaper](http://aka.ms/azsentinelmssp)
   * Great insights on how MSSPs can configure and add value to Sentinel.
* [Azure Sentinel Pricing](https://azure.microsoft.com/en-us/pricing/details/azure-sentinel/)
   * New workspaces can ingest up to 10GB/day of log data for the first 31-days at no cost. Both Log Analytics data ingestion and Microsoft Sentinel charges are waived during the 31-day trial period. This free trial is subject to a 20 workspace limit per Azure tenant. See below for usage steps.
* [Design your Microsoft Sentinel workspace architecture - Decision Tree](https://docs.microsoft.com/en-us/azure/sentinel/design-your-workspace-architecture#decision-tree)


### How to build a demo instance

Use these steps to build a demo instance; should be free for one month – see above

1. [Azure-Sentinel/Solutions/Training/Azure-Sentinel-Training-Lab
at master · Azure/Azure-Sentinel · GitHub](https://github.com/Azure/Azure-Sentinel/tree/master/Solutions/Training/Azure-Sentinel-Training-Lab)
   * Initial setup - includes dummy data
2. [Deploy and monitor Azure Key Vault honeytokens with Microsoft Sentinel](https://docs.microsoft.com/en-us/azure/sentinel/monitor-key-vault-honeytokens?tabs=deploy-at-scale)
   * Optional, but useful
3. [Connect your AWS account to Microsoft Defender for Cloud](https://docs.microsoft.com/en-us/azure/defender-for-cloud/quickstart-onboard-aws?pivots=env-settings)
   * Optional, but useful
4. [Connect security alerts to Microsoft Sentinel - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/connect-defender-for-cloud)
   * Defender for Cloud Connector
5. [Alert validation in Microsoft Defender for Cloud - Microsoft Docs](https://docs.microsoft.com/en-us/azure/defender-for-cloud/alert-validation)
   * Sample security alerts
6. [Send AAD logs to the workspace](https://docs.microsoft.com/en-us/azure/active-directory/reports-monitoring/howto-integrate-activity-logs-with-log-analytics#send-logs-to-azure-monitor)
7. [Connect Azure Active Directory data to Microsoft Sentinel](https://docs.microsoft.com/en-us/azure/sentinel/connect-azure-active-directory)
8. [Connect Microsoft Sentinel to Amazon Web Services to ingest AWS service log data](https://docs.microsoft.com/en-us/azure/sentinel/connect-aws?tabs=ct)
9. [Possible additional dummy data](https://github.com/OTRF/Microsoft-Sentinel2Go)
   * GitHub - OTRF/Microsoft-Sentinel2Go: Microsoft Sentinel2Go is an open source project developed to expedite the deployment of a Microsoft Sentinel research lab.
10. [Sample CEF Data into Azure Sentinel](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/ingest-sample-cef-data-into-azure-sentinel/ba-p/1064158)

## Associate

* [Join the Security Community - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/security-compliance-and-identity/join-our-security-community/ba-p/927888)
* [Azure Sentinel Wiki - GitHub](https://github.com/Azure/Azure-Sentinel/wiki)
* Exam SC-200: Microsoft Security Operations Analyst - Microsoft Docs[](https://docs.microsoft.com/en-us/learn/certifications/exams/sc-200?tab=tab-learning-paths)
* [Workspace architecture best practices for Microsoft Sentinel - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/best-practices-workspace-architecture)
* [Design your Microsoft Sentinel workspace architecture - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/design-your-workspace-architecture)
* [Sample Microsoft Sentinel workspace designs - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/sample-workspace-designs)
* [Azure Network Security Ninja Training - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/azure-network-security-blog/azure-network-security-ninja-training/ba-p/2356101)
* [Microsoft Sentinel introduces enhancements in machine learning and productivity at Ignite 2021 - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/microsoft-sentinel-introduces-enhancements-in-machine-learning/ba-p/2897871)
* [Behind the Scenes: The ML Approach for Detecting Advanced Multistage Attacks with Sentinel Fusion - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/behind-the-scenes-the-ml-approach-for-detecting-advanced/ba-p/3239236)
* [Find your Microsoft Sentinel data connector - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/data-connectors-reference)
* [Resources for creating Microsoft Sentinel custom connectors - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/create-custom-connector#compare-custom-connector-methods)
* [Enrich incidents using entity mapping](https://docs.microsoft.com/en-us/azure/sentinel/entities#entity-mapping)
   * Map the data fields in the various connector tables to Sentinel recognized entities; this will also help when grouping alerts into incidents.
* [Ingest, Archive, Search, and Restore Data in Microsoft Sentinel - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/ingest-archive-search-and-restore-data-in-microsoft-sentinel/ba-p/3195126)




## Expert
* [Azure Sentinel Ninja L400 Training](https://techcommunity.microsoft.com/t5/azure-sentinel/become-an-azure-sentinel-ninja-the-complete-level-400-training/ba-p/1246310)
* [The FAQ companion to the Azure Sentinel Ninja training](https://techcommunity.microsoft.com/t5/azure-sentinel/the-faq-companion-to-the-azure-sentinel-ninja-training/ba-p/2022485)

## Community
* [Security Community Webinars](https://techcommunity.microsoft.com/t5/microsoft-security-and/security-community-webinars/ba-p/927888)

### Build a SOC and operationalize Security Operations

* [What's New: Azure Sentinel - SOC Process Framework Workbook - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/what-s-new-azure-sentinel-soc-process-framework-workbook/ba-p/2339315)
* [SOC Process Framework Overview - YouTube](https://www.youtube.com/watch?v=RnPMwy7AoS0&amp;list=PL3sJcHWKYIVPhCDIdZjVueLIkAfXijylG)

### Agents Resources

* [Overview of the Azure Connected Machine Agent - Azure Arc - Microsoft Docs](https://docs.microsoft.com/en-us/azure/azure-arc/servers/agent-overview)
* [Connect hybrid machines to Azure at scale - Azure Arc - Microsoft Docs](https://docs.microsoft.com/en-us/azure/azure-arc/servers/onboard-service-principal)
* [Install the Azure Monitor agent - Azure Monitor - Microsoft Docs](https://docs.microsoft.com/en-us/azure/azure-monitor/agents/azure-monitor-agent-install?tabs=ARMAgentPowerShell%2CPowerShellWindows%2CPowerShellWindowsArc%2CCLIWindows%2CCLIWindowsArc)
* [Data Collection Rules in Azure Monitor (preview) - Azure Monitor - Microsoft Docs](https://docs.microsoft.com/en-us/azure/azure-monitor/agents/data-collection-rule-overview) 
   * Ability to filter out only the required security data
* [Azure Monitor service limits - Azure Monitor - Microsoft Docs](https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#data-collection-rules)
* [We're retiring the Log Analytics agent in Azure Monitor on 31 August 2024](https://azure.microsoft.com/en-us/updates/were-retiring-the-log-analytics-agent-in-azure-monitor-on-31-august-2024/)

### KQL

* [GitHub - reprise99/Sentinel-Queries: Collection of KQL queries](https://github.com/reprise99/Sentinel-Queries)
* [GitHub - rod-trent/MustLearnKQL: Code included as part of the MustLearnKQL blog series](https://github.com/rod-trent/MustLearnKQL)
* [KQL Cheat Sheet — MB Secure](https://www.mbsecure.nl/blog/2019/12/kql-cheat-sheet)
* [Advanced KQL Framework Workbook - Empowering you to become KQL-savvy - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/advanced-kql-framework-workbook-empowering-you-to-become-kql/ba-p/3033766)

### ADX

[Start for free using Azure Data Explorer - Microsoft Docs](https://docs.microsoft.com/en-us/azure/data-explorer/start-for-free)
   * Free cluster, you just need a Microsoft Identity. 100GB, up to 10 DBs, up to 100 tables per DB, up to 200 columns per table. Free for 1 year, but can be extended.

### Notebooks

* [Getting started with Azure Sentinel Notebooks](https://www.youtube.com/watch?v=TgRRJeoyAYw&feature=youtu.be) video 
* [Azure Sentinel notebook ninja - the series! (microsoft.com)](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/becoming-a-microsoft-sentinel-notebooks-ninja-the-series/ba-p/2693491)
* [GitHub - Azure/Azure-Sentinel-Notebooks at 7402ad1fc35fc78c05c51fe068ea547f928000af](https://github.com/Azure/Azure-Sentinel-Notebooks/tree/7402ad1fc35fc78c05c51fe068ea547f928000af)
* [Azure-Sentinel-Notebooks/Training - MSTICPy Training 1221.ipynb at master · Azure/Azure-Sentinel-Notebooks · GitHub](https://github.com/Azure/Azure-Sentinel-Notebooks/blob/master/Sample-Notebooks/Training%20-%20MSTICPy%20Training%201221.ipynb)
* [Getting Started — msticpy 1.5.0 documentation](https://msticpy.readthedocs.io/en/latest/GettingStarted.html)
* [Infosec Jupyterthon!](https://infosecjupyterthon.com/introduction.html)
* [MSTICPy January 2022 Hackathon · microsoft/msticpy Wiki · GitHub](https://github.com/microsoft/msticpy/wiki/MSTICPy-January-2022-Hackathon)

### Migration

* [Best practices for migrating detection rules from ArcSight, Splunk and QRadar to Azure Sentinel - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/best-practices-for-migrating-detection-rules-from-arcsight/ba-p/2216417)
* [Uncoder.IO - Universal Sigma Rule Converter for SIEM, EDR, and NTDR](https://uncoder.io/)
* [Azure-Sentinel/Tools/RuleMigration at master · Azure/Azure-Sentinel (github.com)](https://github.com/Azure/Azure-Sentinel/tree/master/Tools/RuleMigration)
* [Moving to next-generation SIEM with Azure Sentinel (microsoft.com)](https://www.microsoft.com/en-us/insidetrack/moving-to-next-generation-siem-with-azure-sentinel) – our internal migration story
* [Boosting Microsoft’s response to cybersecurity attacks with Microsoft Azure Sentinel - Inside Track Blog](https://www.microsoft.com/insidetrack/blog/boosting-microsofts-response-to-cybersecurity-attacks-with-microsoft-azure-sentinel/) – our internal migration story
* [Azure Sentinel Side-by-Side with QRadar - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/azure-sentinel-side-by-side-with-qradar/ba-p/1488333)
* [Azure Sentinel Side-by-Side with Splunk - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/azure-sentinel-side-by-side-with-splunk/ba-p/1211266)
* [Sending enriched Microsoft Sentinel alerts to 3rd party SIEM and Ticketing Systems - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/sending-enriched-microsoft-sentinel-alerts-to-3rd-party-siem-and/ba-p/1456976)

### Build Solutions and other Contributions

* [Introducing Microsoft Sentinel Content hub! - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/introducing-microsoft-sentinel-content-hub/ba-p/2928102#:~:text=Content%20hub%20provides%20centralized%20in-product%20discoverability%2C%20single-step%20deployment%2C,available%20in%20the%20solutions%20gallery%20plus%20much%20more.) – creating packaged solutions
* [https://aka.ms/sentinelsolutionsbuildguide](https://aka.ms/sentinelsolutionsbuildguide) - A guide provides an overview of Microsoft Sentinel solutions, and how to build and publish a solution for Microsoft Sentinel.
* [https://aka.ms/threathunters](https://aka.ms/threathunters) - Solutions, Playbooks, Workbooks, Hunting, etc.

### Risk IQ Integration

* [RiskIQ Illuminate Content hub solution within Microsoft Sentinel – My Faber Security](https://myfabersecurity.com/2022/03/04/riskiq-illuminate-content-hub-solution-within-microsoft-sentinel/)
   * Solution under Content Hub **RiskIQ Illuminate**. Reference: [Azure-Sentinel/Solutions/RiskIQ/Playbooks at a18c064b8016db9c7f01c8e856c6c13c98e712d0 - Azure/Azure-Sentinel (github.com)](https://github.com/Azure/Azure-Sentinel/tree/a18c064b8016db9c7f01c8e856c6c13c98e712d0/Solutions/RiskIQ/Playbooks)
   * As the link states, you have to request a [trial key](https://community.riskiq.com/home) (see [account settings](https://community.riskiq.com/settings)). The trial takes a little while to kick in, so if you get a 402 error while testing, just wait a little longer to test.

### Repositories

* [Enable Continuous Deployment Natively with Microsoft Sentinel Repositories! - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/enable-continuous-deployment-natively-with-microsoft-sentinel/ba-p/2929413)
* [Microsoft-Sentinel-As-A-Code: Export Microsoft Sentinel artifacts like Analytical Rules, Hunting Queries, Workbooks in order to support new feature Repositories CI/CD Pipeline](https://github.com/sreedharande/Microsoft-Sentinel-As-A-Code)

### Other Useful Information for Partners

#### Storage options

* [MSSP Whitepaper](http://aka.ms/azsentinelmssp)
   * Azure Log Analytics/Azure Sentinel
   * Azure Data Explorer (ADX) – less expensive - but same KQL queries, no UEBA, no visual investigation, less performance
   * Azure Blob Storage – least expensive – query using **_externaldata_** operator in KQL
   * ADX and Blob Storage combined – best of both worlds – data in storage, but you can run KQL queries – you create an **external table in ADX** that points to the whole container (blob storage)
   * **NEW** - [Ingest, Archive, Search, and Restore Data in Microsoft Sentinel - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/ingest-archive-search-and-restore-data-in-microsoft-sentinel/ba-p/3195126)
      * Logs that can work as Basic Logs rather than Analytics Logs are flipped to Basic Logs (Basic Logs are 60% cheaper)
      * Data can be archived from Basic Logs and Analytics logs to Archive (cold) storage. (Logs in cold storage are 80% cheaper than retention in the log analytics database)
      * When needed for forensic and audit reasons, archive data is rehydrated so it can be searched. (Pay-to-use for each search of archived data.)
   * NEW - [Microsoft Sentinel Support for Ingestion-Time Data Transformations - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/microsoft-sentinel-support-for-ingestion-time-data/ba-p/3244531)
      * Ingestion time transformations and Data Collection Rules (DCR)-based custom logs
      * Cost reduction - using ingestion time transformations, customers can now filter out data which is irrelevant to security analysis.
      * [Library of Transformations](http://aka.ms/sentinel-transforms)

#### Cost calculator

* [Sentinel Cost Calculator](https://cloudpartners.transform.microsoft.com/download?assetname=assets/Azure_Sentinel_Calculator.xlsx&download=1)
* [Azure Data Explorer Cost Calculator](https://dataexplorer.azure.com/AzureDataExplorerCostEstimator.html)

#### Some data at **no cost:**

* Azure Sentinel and Log Analytics offer ingestion & 90 day retention of some data at no cost. Those include:
   * Azure Activity Logs
   * Office 365 Audit Logs (all SharePoint, Exchange admin activity, Teams)
   * Alerts from Microsoft Defender products: Defender for Cloud, Microsoft 365 Defender, Microsoft Defender for Office 365, Microsoft Defender for Identity, Microsoft Defender for Endpoint, Microsoft Defender for Cloud Apps and Azure Information Protection
   * Azure Information Protection alerts (when available)
   * Defender for IOT (alert)

REF: [Plan and manage costs for Microsoft Sentinel - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/billing#free-data-sources)

#### Other ways to save $:

* Commitment tiers (previously capacity reservations) – can save up to 65% compared to pay-as-you-go ([Azure Sentinel Pricing - Microsoft Azure](https://azure.microsoft.com/en-us/pricing/details/azure-sentinel/))
* [Microsoft 365 E5 benefit offer with Azure Sentinel - Microsoft Azure](https://azure.microsoft.com/en-us/offers/sentinel-microsoft-365-offer/) - Save up to USD1500/month on a typical 3,500 seat deployment -- Microsoft 365 E5, A5, F5, G5 and Microsoft 365 E5, A5, F5, G5 Security customers can receive a data grant of up to 5MB per user/day to ingest Microsoft 365 data. Summary [here](https://azurecloudai.blog/2021/11/16/the-short-takes-version-of-the-updated-microsoft-sentinel-trial-and-customer-benefit-offers/). Data sources:
   * Azure Active Directory (Azure AD) sign-in and audit logs
   * Microsoft Cloud App Security shadow IT discovery logs
   * Microsoft Information Protection logs
   * Microsoft 365 advanced hunting data
* [How to Locate the Microsoft Sentinel Free Benefit in Cost Management + Billing – Azure Cloud & AI Domain Blog (azurecloudai.blog)](https://azurecloudai.blog/2022/03/15/how-to-locate-the-microsoft-sentinel-free-benefit-in-cost-management-billing/)
* [Using the Microsoft Sentinel Cost Workbook – Azure Cloud & AI Domain Blog (azurecloudai.blog)](https://azurecloudai.blog/2021/12/01/using-the-microsoft-sentinel-cost-workbook/)
* [We're retiring the Log Analytics agent in Azure Monitor on 31 August 2024 - Azure updates - Microsoft Azure](https://azure.microsoft.com/en-us/updates/were-retiring-the-log-analytics-agent-in-azure-monitor-on-31-august-2024/) – The ability to use [data collection rules](https://docs.microsoft.com/en-us/azure/azure-monitor/agents/data-collection-rule-overview) means not all data has to be sent, only the required filtered data.
* Free Trial - [Azure Sentinel Pricing - Microsoft Azure](https://azure.microsoft.com/en-us/pricing/details/azure-sentinel/) - New workspaces can ingest up to 10GB/day of log data for the first 31-days at no cost. Both Log Analytics data ingestion and Microsoft Sentinel charges are waived during the 31-day trial period. This free trial is subject to a 20 workspace limit per Azure tenant.

### Overall Security Info for Partners

* Intro is the MCRA (https://aka.ms/mcra) - [Microsoft Cybersecurity Reference Architectures - Security documentation - Microsoft Docs](https://docs.microsoft.com/en-us/security/cybersecurity-reference-architecture/mcra)
* See the associated videos here: [MCRA Intro - YouTube](https://www.youtube.com/watch?v=6iYxNm3TOiI&list=PLtVMyW0H7aiOQwZSsn2d-tg2z729ce1BZ) – these videos go over every slide in the MCRA deck.
* [Join Our Security Community - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/security-compliance-and-identity/join-our-security-community/ba-p/927888)
* [M365 Accelerator Program (m365partneraccelerator.azurewebsites.net)](https://m365partneraccelerator.azurewebsites.net/)
* Partners can [sign up for the ongoing Cloud Security Private Community program](https://www.aka.ms/prseccom), and will receive access to our NDA roadmap calls, design exercises, surveys, and private previews. Note: Partners must have a valid NDA with Microsoft to be able to sign up for this program.
* [Offer listing best practices - Microsoft commercial marketplace - Microsoft Docs](https://docs.microsoft.com/en-us/azure/marketplace/gtm-offer-listing-best-practices) and [Marketing best practices - Microsoft commercial marketplace - Microsoft Docs](https://docs.microsoft.com/en-us/azure/marketplace/gtm-marketing-best-practices)

