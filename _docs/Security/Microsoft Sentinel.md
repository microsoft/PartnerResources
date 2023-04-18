---
layout: page
title: Microsoft Sentinel
description: Resources for Microsoft Sentinel
updated: 2023-02-13
permalink: /security/microsoft-sentinel
tags:
- security
- learning plan
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
* [Microsoft Sentinel Skill-up Training - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/skill-up-resources)
* [Design your Microsoft Sentinel Workspace Architecture - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/design-your-workspace-architecture#decision-tree)


#### Building a Demo. Instance
Use these steps to build a demo instance; free for one month

1. [Microsoft Sentinel Training Lab](https://github.com/Azure/Azure-Sentinel/tree/master/Solutions/Training/Azure-Sentinel-Training-Lab)
   * Initial Setup ("Dummy Data")
2. [Connect Azure Active Directory (Azure AD) Data to Microsoft Sentinel - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/connect-azure-active-directory)
3. [Possible Additional Data](https://github.com/OTRF/Microsoft-Sentinel2Go)
   * Microsoft Sentinel To-Go is an open source project developed to expedite the deployment of a Microsoft Sentinel lab along with other resources for research purposes. (i.e., more "Dummy Data")
4. [Ingest Sample CEF Data into Sentinel - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/ingest-sample-cef-data-into-azure-sentinel/ba-p/1064158)
   * Sample Data CEF
5. [Additional Microsoft Sentinel Sample Data](https://github.com/Yaniv-Shasha/Sentinel/tree/master/Sample_Data)
6. [New Ingestion SampleData-as-a-Service Solution - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/new-ingestion-sampledata-as-a-service-solution-for-a-great-demos/ba-p/3598500)

## Associate
* [Microsoft Sentinel Workspace Architecture Best Practices  - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/best-practices-workspace-architecture)
* [Microsoft Sentinel Sample Workspace Designs - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/sample-workspace-designs)
* [Microsoft 365 Defender Integration with Microsoft Sentinel - Microsoft Docs](https://learn.microsoft.com/en-us/microsoft-365/security/defender/microsoft-365-defender-integration-with-azure-sentinel?view=o365-worldwide)
* [Find your Microsoft Sentinel Data Connector - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/data-connectors-reference)
* [Resources for Creating Microsoft Sentinel Custom Connectors - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/create-custom-connector#compare-custom-connector-methods)
* [Become a Microsoft Sentinel Automation Ninja - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/become-a-microsoft-sentinel-automation-ninja/ba-p/3563377)
* [Become a Microsoft Sentinel Ninja: The complete level 400 training](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/become-a-microsoft-sentinel-ninja-the-complete-level-400/ba-p/1246310)


#### Azure Lighthouse
* [Delegate Access using Azure Lighthouse for a Sentinel POC - My Faber Security](https://myfabersecurity.com/2022/07/15/delegate-access-using-azure-lighthouse-for-a-sentinel-poc/)
* [Azure Lighthouse & Microsoft Sentinel: Assigning Access to Managed Identities in Customer Tenant - My Faber Security](https://myfabersecurity.com/2022/08/31/azure-lighthouse-and-sentinel-assigning-access-to-managed-identities-in-the-customer-tenant/)

#### Build a SOC & Operationalize Security Operations
* [What's New: Azure Sentinel - SOC Process Framework Workbook - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/what-s-new-azure-sentinel-soc-process-framework-workbook/ba-p/2339315)
* [SOC Process Framework Overview - YouTube](https://www.youtube.com/watch?v=RnPMwy7AoS0&amp;list=PL3sJcHWKYIVPhCDIdZjVueLIkAfXijylG)
* [Best Practices for Microsoft Sentinel - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/best-practices)
* [Protecting MSSP Intellectual Property in Microsoft Sentinel - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/mssp-protect-intellectual-property)
* [MSSPs and Identity - Considerations for tenant architecture and delegating access to SOC analysts](https://myfabersecurity.com/2023/01/11/mssps-and-identity/)

#### Agents Resources
* [Migrate to Azure Monitor Agent for better Security, Reliability and Management - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/azure-observability-blog/migrate-to-azure-monitor-agent-for-better-security-reliability/ba-p/3609810)
* [Overview of the Azure Connected Machine Agent (Azure Arc) - Microsoft Docs](https://learn.microsoft.com/en-us/azure/azure-arc/servers/agent-overview)
* [Connect Hybrid Machines to Azure at Scale (Azure Arc) -  Microsoft Docs](https://learn.microsoft.com/en-us/azure/azure-arc/servers/onboard-service-principal)
* [Azure Monitor Agent Overview - Microsoft Docs](https://learn.microsoft.com/en-us/azure/azure-monitor/agents/agents-overview)
* [Data Collection Rules in Azure Monitor - Microsoft Docs](https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/data-collection-rule-overview)
* [Sentinel Syslog Forwarder with AMA](https://starkonsec.com/2022/04/18/sentinel-syslog-forwarder-with-the-azure-monitor-agent/)
* [Azure Monitor Agent Migration (Remove Log Analytics Agent) Lab](https://github.com/Azure/Microsoft-Defender-for-Cloud/tree/main/Powershell%20scripts/Remove%20Log%20Analytics%20Agent%20At%20Scale)

#### KQL
* [KQL for Microsoft Sentinel Lab & Queries](https://github.com/reprise99/Sentinel-Queries)
* [MustLearnKQL Blog Series](https://github.com/rod-trent/MustLearnKQL)
* [KQL Cheat Sheet](https://www.mbsecure.nl/blog/2019/12/kql-cheat-sheet)
* [Advanced KQL Framework Workbook - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/advanced-kql-framework-workbook-empowering-you-to-become-kql/ba-p/3033766)
* [KQL Search](https://www.kqlsearch.com)
* [SQL to KQL Cheat sheet](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/sqlcheatsheet)

#### ADX
   * [What is a free Azure Data Explorer Cluster? - Microsoft Docs](https://docs.microsoft.com/en-us/azure/data-explorer/start-for-free)
      * Free cluster, only a Microsoft Identity is required
   * [Azure Data Explorer in 60 minutes with Samples - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/azure-data-explorer-blog/azure-data-explorer-in-60-minutes-with-the-new-samples-gallery/ba-p/3447552)

#### Notebooks
* [Becoming a Microsoft Sentinel Notebooks Ninja - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/becoming-a-microsoft-sentinel-notebooks-ninja-the-series/ba-p/2693491)
* [Azure Sentinel Notebooks Lab](https://github.com/Azure/Azure-Sentinel-Notebooks/tree/7402ad1fc35fc78c05c51fe068ea547f928000af)
* [Get Started with Jupyter Notebooks & MSTICPy in Microsoft Sentinel - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/notebook-get-started)
* [Detect Masqueraded Process Name Anomalies with ML Notebook - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/detect-masqueraded-process-name-anomalies-using-an-ml-notebook/ba-p/3596405)
* [Hunting for Low & Slow Password Sprays Using Machine Learning - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/hunting-for-low-and-slow-password-sprays-using-machine-learning/ba-p/3592052)
* [Hunting for Teams Phishing with Microsoft Sentinel, Defender, Microsoft Graph and MSTICPy - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/hunting-for-teams-phishing-with-microsoft-sentinel-defender/ba-p/3601746)

#### Migration
* [Plan Migration to Microsoft Sentinel - Microsoft Docs](https://docs.microsoft.com/en-us/azure/sentinel/migration)
* [Microsoft Sentinel Migration: Select Target Azure Platform for Exported Data - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/migration-ingestion-target-platform)
* [Microsoft Sentinel Migration: Select Data Ingestion Tool - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/migration-ingestion-tool)
* [Unicoder Sigma Rule Converter for SIEM, EDR, & NTDR](https://uncoder.io/)
* [Microsoft Sentinel Repository](https://github.com/Azure/Azure-Sentinel)
* [Azure Sentinel Side-by-Side with QRadar](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/azure-sentinel-side-by-side-with-qradar/ba-p/1488333)
* [Azure Sentinel Side-by-Side with Splunk](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/azure-sentinel-side-by-side-with-splunk/ba-p/1211266)

#### Build Solutions & Other Contributions
* [Guide to Building Microsoft Sentinel Solutions](https://github.com/Azure/Azure-Sentinel/tree/master/Solutions#guide-to-building-microsoft-sentinel-solutions)

#### MDTI (Defender for Threat Intelligence) & Risk IQ Integration
* [Become a Microsoft Defender Threat Intelligence Ninja - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-defender-threat/become-a-microsoft-defender-threat-intelligence-ninja-the/ba-p/3656965)
* [Performing a Successful Proof of Concept (PoC)](https://techcommunity.microsoft.com/t5/microsoft-defender-threat/performing-a-successful-proof-of-concept-poc/ba-p/3742412)
* [New Threat Intelligence Features in Microsoft Sentinel - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/new-threat-intelligence-features-in-microsoft-sentinel/ba-p/3585214)
* [Infrastructure Chaining with Microsoft Defender Threat Intelligence - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-defender-threat/infrastructure-chaining-with-microsoft-defender-threat/ba-p/3687956)
* [RiskIQ Illuminate Content Hub Solution within Microsoft Sentinel – My Faber Security](https://myfabersecurity.com/2022/03/04/riskiq-illuminate-content-hub-solution-within-microsoft-sentinel/)

#### SOAR
* [Microsoft Sentinel Automation Tips & Tricks - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/microsoft-sentinel-automation-tips-amp-tricks-part-1-automation/ba-p/3558454)
* [Safely Integrate Playbooks with Custom APIs with no Pre-built Logic App Connector - My Faber Security](https://myfabersecurity.com/2022/11/21/safely-integrate-playbooks-with-custom-apis-when-there-is-no-pre-built-logic-app-connector/)

#### Repositories
* [Enable Continuous Deployment Natively with Microsoft Sentinel Repositories - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/enable-continuous-deployment-natively-with-microsoft-sentinel/ba-p/2929413)
* [Microsoft Sentinel As-A-Code Lab](https://github.com/sreedharande/Microsoft-Sentinel-As-A-Code)
* [Sample Content Repository](https://github.com/SentinelCICD/RepositoriesSampleContent)
* [Customize Repository Deployments - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/ci-cd-custom-deploy?tabs=github)

#### Fusion
* [Behind the Scenes: The ML Approach for Detecting Advanced Multistage Attacks with Sentinel Fusion - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/behind-the-scenes-the-ml-approach-for-detecting-advanced/ba-p/3239236)
* [Advanced Multistage Attack Detection in Microsoft Sentinel - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/fusion)

#### UEBA
* [Discover the Power of UEBA Anomalies in Microsoft Sentinel - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/discover-the-power-of-ueba-anomalies-in-microsoft-sentinel/ba-p/3576185)
* [Microsoft Sentinel Customizable Ml Based Anomalies now Generally Available - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/microsoft-sentinel-customizable-machine-learning-based-anomalies/ba-p/3624436)

#### Storage options
* [Refer to Microsoft Sentinel Technical Playbook for MSSPs](http://aka.ms/azsentinelmssp)

#### Costs
* [Refer to Microsoft Sentinel Pricing](https://azure.microsoft.com/en-us/pricing/details/microsoft-sentinel/)
* [Microsoft Sentinel Cost Calculator](https://cloudpartners.transform.microsoft.com/download?assetname=assets/Azure_Sentinel_Calculator.xlsx&download=1)
* [Azure Data Explorer (Kusto) Cost Estimator](https://dataexplorer.azure.com/AzureDataExplorerCostEstimator.html)

#### Data at No-Cost
Microsoft Sentinel and Log Analytics offer ingestion & 90-day retention of *some* data at no cost, including:
   * Azure Activity Logs
   * Office 365 Audit Logs (e.g., SharePoint activity, Exchange activity, Teams)
   * Alerts from Microsoft Defender products
   * Azure Information Protection Alerts
   * Microsoft Defender for IoT Alerts

Reference [Plan Costs and Microsoft Sentinel Pricing and Billing - Microsoft Docs](https://learn.microsoft.com/en-us/azure/sentinel/billing?tabs=commitment-tier) for further information.

#### Other Ways to Save
* [Microsoft Sentinel Benefit for Microsoft 365 E5, A5, F5, and G5 Customers](https://azure.microsoft.com/en-us/offers/sentinel-microsoft-365-offer/#:~:text=Microsoft%20Sentinel%20benefit%20for%20Microsoft%20365%20E5%2C%20A5%2C,scale.%204%20Enable%20efficient%20and%20effective%20response%20) 
* [Locate Microsoft Sentinel Free Benefit in Cost Management & Billing](https://azurecloudai.blog/2022/03/15/how-to-locate-the-microsoft-sentinel-free-benefit-in-cost-management-billing/)
* Commitment Tiers; save up to 65% compared to pay-as-you-go.
