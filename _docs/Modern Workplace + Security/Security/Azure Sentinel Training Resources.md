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




## Expert
* [Azure Sentinel Ninja L400 Training](https://techcommunity.microsoft.com/t5/azure-sentinel/become-an-azure-sentinel-ninja-the-complete-level-400-training/ba-p/1246310)
* [The FAQ companion to the Azure Sentinel Ninja training](https://techcommunity.microsoft.com/t5/azure-sentinel/the-faq-companion-to-the-azure-sentinel-ninja-training/ba-p/2022485)

## Community
* [Security Community Webinars](https://techcommunity.microsoft.com/t5/microsoft-security-and/security-community-webinars/ba-p/927888)

------------------

Sentinel Ramp-Up
Begin here:
* Become a Microsoft Sentinel Ninja: The complete level 400 training - Microsoft Tech Community
* MSSP Whitepaper: http://aka.ms/azsentinelmssp - great insights on how MSSPs can configure and add value to Sentinel.
* Free Trial - Azure Sentinel Pricing | Microsoft Azure - New workspaces can ingest up to 10GB/day of log data for the first 31-days at no cost. Both Log Analytics data ingestion and Microsoft Sentinel charges are waived during the 31-day trial period. This free trial is subject to a 20 workspace limit per Azure tenant. – This is what I use to build my demo instance, see the steps I use below.
* Design your Microsoft Sentinel workspace architecture | Microsoft Docs – decision tree
How I build my demo instance (good for a month to keep it free of charge – see above): 
1. Azure-Sentinel/Solutions/Training/Azure-Sentinel-Training-Lab at master · Azure/Azure-Sentinel · GitHub – Initial setup - includes dummy data
2. Deploy and monitor Azure Key Vault honeytokens with Microsoft Sentinel - Optional, but useful
3. Connect your AWS account to Microsoft Defender for Cloud- Optional, but useful
4. Connect security alerts to Microsoft Sentinel | Microsoft Docs – Defender for Cloud connector
5. Alert validation in Microsoft Defender for Cloud | Microsoft Docs – sample security alerts
6. Send AAD logs to the workspace you configured on step 1.
7. Connect Azure Active Directory data to Microsoft Sentinel – 
8. Connect Microsoft Sentinel to Amazon Web Services to ingest AWS service log data 
9. Possible additional dummy data: GitHub - OTRF/Microsoft-Sentinel2Go: Microsoft Sentinel2Go is an open source project developed to expedite the deployment of a Microsoft Sentinel research lab.
10. Sample data CEF - Ingest Sample CEF data into Azure Sentinel - Microsoft Tech Community
Additional Sentinel Learning and Architecting Resources:
* Join Our Security Community - Microsoft Tech Community
* Home · Azure/Azure-Sentinel Wiki (github.com)
* Exam SC-200: Microsoft Security Operations Analyst - Learn | Microsoft Docs
* Workspace architecture best practices for Microsoft Sentinel | Microsoft Docs
* Design your Microsoft Sentinel workspace architecture | Microsoft Docs
* Sample Microsoft Sentinel workspace designs | Microsoft Docs
* Azure Network Security Ninja Training - Microsoft Tech Community
* Microsoft Sentinel introduces enhancements in machine learning and productivity at Ignite 2021 - Microsoft Tech Community
* Behind the Scenes: The ML Approach for Detecting Advanced Multistage Attacks with Sentinel Fusion - Microsoft Tech Community
* Find your Microsoft Sentinel data connector | Microsoft Docs
* Resources for creating Microsoft Sentinel custom connectors | Microsoft Docs
* Enrich incidents using entity mapping to map the data fields in the various connector tables to Sentinel recognized entities, this will also help when grouping alerts into incidents.
* Ingest, Archive, Search, and Restore Data in Microsoft Sentinel - Microsoft Tech Community

 Build a SOC and operationalize Security Operations 
* What's New: Azure Sentinel - SOC Process Framework Workbook - Microsoft Tech Community and associated videos 1 SOC Process Framework Overview Final - YouTube
Agents Useful Resources: 
* Overview of the Azure Connected Machine agent - Azure Arc | Microsoft Docs
* Connect hybrid machines to Azure at scale - Azure Arc | Microsoft Docs
* Install the Azure Monitor agent - Azure Monitor | Microsoft Docs
* Data Collection Rules in Azure Monitor (preview) - Azure Monitor | Microsoft Docs – ability to filter out only the required security data
* Azure Monitor service limits - Azure Monitor | Microsoft Docs
* We're retiring the Log Analytics agent in Azure Monitor on 31 August 2024 | Azure updates | Microsoft Azure
KQL
* GitHub - reprise99/Sentinel-Queries: Collection of KQL queries
* GitHub - rod-trent/MustLearnKQL: Code included as part of the MustLearnKQL blog series
* KQL Cheat Sheet — MB Secure
* Advanced KQL Framework Workbook - Empowering you to become KQL-savvy - Microsoft Tech Community
ADX
* Start for free using Azure Data Explorer. | Microsoft Docs – free cluster, you just need a Microsoft Identity. 100GB, up to 10 DBs, up to 100 tables per DB, up to 200 columns per table. Free for 1 year, but can be extended. 
Notebooks
* Getting started with Azure Sentinel Notebooks video 
* Azure Sentinel notebook ninja - the series! (microsoft.com)
* GitHub - Azure/Azure-Sentinel-Notebooks at 7402ad1fc35fc78c05c51fe068ea547f928000af
* Azure-Sentinel-Notebooks/Training - MSTICPy Training 1221.ipynb at master · Azure/Azure-Sentinel-Notebooks · GitHub
* Getting Started — msticpy 1.5.0 documentation
* Infosec Jupyterthon!
* MSTICPy January 2022 Hackathon · microsoft/msticpy Wiki · GitHub
Migration
* Best practices for migrating detection rules from ArcSight, Splunk and QRadar to Azure Sentinel - Microsoft Tech Community 
* Uncoder.IO | Universal Sigma Rule Converter for SIEM, EDR, and NTDR
* Azure-Sentinel/Tools/RuleMigration at master · Azure/Azure-Sentinel (github.com)
* Moving to next-generation SIEM with Azure Sentinel (microsoft.com) – our internal migration story
* Boosting Microsoft’s response to cybersecurity attacks with Microsoft Azure Sentinel - Inside Track Blog – our internal migration story
* Azure Sentinel Side-by-Side with QRadar - Microsoft Tech Community
* Azure Sentinel Side-by-Side with Splunk - Microsoft Tech Community
* Sending enriched Microsoft Sentinel alerts to 3rd party SIEM and Ticketing Systems - Microsoft Tech Community
Build Solutions and other Contributions
* Introducing Microsoft Sentinel Content hub! - Microsoft Tech Community – creating packaged solutions
* https://aka.ms/sentinelsolutionsbuildguide - A guide provides an overview of Microsoft Sentinel solutions, and how to build and publish a solution for Microsoft Sentinel.
* https://aka.ms/threathunters - Solutions, Playbooks, Workbooks, Hunting, etc. 
Risk IQ Integration (current)
* RiskIQ Illuminate Content hub solution within Microsoft Sentinel – My Faber Security
o Solution under Content Hub “RiskIQ Illuminate”. Reference: Azure-Sentinel/Solutions/RiskIQ/Playbooks at a18c064b8016db9c7f01c8e856c6c13c98e712d0 · Azure/Azure-Sentinel (github.com)
o As the link states, you have to request a trial key (see account settings). The trial takes a little while to kick in, so if you get a 402 error while testing, just wait a little longer to test.
Repositories (Automation)
* Enable Continuous Deployment Natively with Microsoft Sentinel Repositories! - Microsoft Tech Community
* Microsoft-Sentinel-As-A-Code: Export Microsoft Sentinel artifacts like Analytical Rules, Hunting Queries, Workbooks in order to support new feature Repositories CI/CD Pipeline

Other Useful Information for Partners:
Storage options:
See the MSSP Whitepaper for more details: http://aka.ms/azsentinelmssp
- Azure Log Analytics/Azure Sentinel
- Azure Data Explorer (ADX) – less expensive -  but same KQL queries, no UEBA, no visual investigation, less performance
- Azure Blob Storage – least expensive – query using externaldata operator in KQL
- ADX and Blob Storage combined – best of both worlds – data in storage, but you can run KQL queries – you create an external table in ADX that points to the whole container (blob storage)
- NEW - Ingest, Archive, Search, and Restore Data in Microsoft Sentinel - Microsoft Tech Community 
o Logs that can work as Basic Logs rather than Analytics Logs are flipped to Basic Logs (Basic Logs are 60% cheaper) 
o Data can be archived from Basic Logs and Analytics logs to Archive (cold) storage. (Logs in cold storage are 80% cheaper than retention in the log analytics database) 
o When needed for forensic and audit reasons, archive data is rehydrated so it can be searched. (Pay-to-use for each search of archived data.)
- NEW - Microsoft Sentinel Support for Ingestion-Time Data Transformations - Microsoft Tech Community
o Ingestion time transformations and Data Collection Rules (DCR)-based custom logs
o Cost reduction - using ingestion time transformations, customers can now filter out data which is irrelevant to security analysis.
o http://aka.ms/sentinel-transforms - library of transformations

Cost calculator: 
- https://cloudpartners.transform.microsoft.com/download?assetname=assets/Azure_Sentinel_Calculator.xlsx&download=1
- https://dataexplorer.azure.com/AzureDataExplorerCostEstimator.html

Some data at no cost:
Azure Sentinel and Log Analytics offer ingestion & 90 day retention of some data at no cost. Those include: 
• Azure Activity Logs
• Office 365 Audit Logs (all SharePoint, Exchange admin activity, Teams)
• Alerts from Microsoft Defender products: Defender for Cloud, Microsoft 365 Defender, Microsoft Defender for Office 365, Microsoft Defender for Identity, Microsoft Defender for Endpoint, Microsoft Defender for Cloud Apps and Azure Information Protection
• Azure Information Protection alerts (when available)
• Defender for IOT (alert)
REF: Plan and manage costs for Microsoft Sentinel | Microsoft Docs
Other ways to save $:
- Commitment tiers (previously capacity reservations) – can save up to 65% compared to pay-as-you-go (Azure Sentinel Pricing | Microsoft Azure)
- Microsoft 365 E5 benefit offer with Azure Sentinel | Microsoft Azure - Save up to USD1500/month on a typical 3,500 seat deployment -- Microsoft 365 E5, A5, F5, G5 and Microsoft 365 E5, A5, F5, G5 Security customers can receive a data grant of up to 5MB per user/day to ingest Microsoft 365 data. Summary here. Data sources:
o Azure Active Directory (Azure AD) sign-in and audit logs
o Microsoft Cloud App Security shadow IT discovery logs
o Microsoft Information Protection logs
o Microsoft 365 advanced hunting data
How to Locate the Microsoft Sentinel Free Benefit in Cost Management + Billing – Azure Cloud & AI Domain Blog (azurecloudai.blog)
- Using the Microsoft Sentinel Cost Workbook – Azure Cloud & AI Domain Blog (azurecloudai.blog)
- We're retiring the Log Analytics agent in Azure Monitor on 31 August 2024 | Azure updates | Microsoft Azure – The ability to use data collection rules means not all data has to be sent, only the required filtered data.
- Free Trial - Azure Sentinel Pricing | Microsoft Azure - New workspaces can ingest up to 10GB/day of log data for the first 31-days at no cost. Both Log Analytics data ingestion and Microsoft Sentinel charges are waived during the 31-day trial period. This free trial is subject to a 20 workspace limit per Azure tenant.


Overall Security Info for Partners:
* Best Intro is the MCRA (https://aka.ms/mcra) - Microsoft Cybersecurity Reference Architectures - Security documentation | Microsoft Docs
* See the associated videos here: MCRA Intro - YouTube – these videos go over every slide in the MCRA deck. 
* Join Our Security Community - Microsoft Tech Community
* M365 Accelerator Program (m365partneraccelerator.azurewebsites.net)
* Partners can sign up for the ongoing Cloud Security Private Community program, and will receive access to our NDA roadmap calls, design exercises, surveys, and private previews. Note: Partners must have a valid NDA with Microsoft to be able to sign up for this program.
* Offer listing best practices - Microsoft commercial marketplace | Microsoft Docs and Marketing best practices - Microsoft commercial marketplace | Microsoft Docs
