---
layout: page
title: Security Certifications
description: Resources for Security Certifications
updated: 2022-07-20
permalink: /modern-workplace/security/security-certifications
tags:
- learning plan
- modern workplace
- security
- Certifications
- SC-200
- SC-300
- SC-400
---

# Security Certifications

Below you will find information about some of the security certifications that are critical for you. Please use the navigation pane on the right to quickly jump between sections or specific certification that you are interested in.

## Microsoft Security Operations Analyst (SC-200)

### Exam Overview

* Mitigate threats using Microsoft 365 Defender (25-30%)
* Mitigate threats using Azure Defender (25-30%)
* Mitigate threats using Azure Sentinel (40-45%)

### Module 1 (Part 1)

* Detect, investigate, respond, and remediate endpoint threats by using Microsoft Defender for Endpoint 
	* Manage data retention, alert notification, and advanced features 
	* Configure device attack surface reduction rules 
	* Configure and manage custom detections and alerts
	* Respond to incidents and alerts 
	* Manage automated investigations and remediations 

* Assess and recommend endpoint configurations to reduce and remediate vulnerabilities by using Microsoft’s Threat and Vulnerability Management solution. 
	* Manage Microsoft Defender for Endpoint threat indicators 
	* Analyze Microsoft Defender for Endpoint threat analytics 

* Manage cross-domain investigations in Microsoft 365 Defender portal 
	* Manage incidents across Microsoft 365 Defender products 
	* Manage actions pending approval across products 
	* Perform advanced threat hunting

### Module 1 (Part 2)

* Detect, investigate, respond, and remediate threats to the productivity environment by using Microsoft Defender for Office 365 
	* Detect, investigate, respond, remediate Microsoft Teams, sharepoint, and onedrive for Business threats 
	* Detect, investigate, respond, remediate threats to email by using Defender for Office 365 
	* Manage data loss prevention policy alerts 
	* Assess and recommend sensitivity labels 
	* Assess and recommend insider risk policies 

* Detect, investigate, respond, and remediate identity threats 
	* Identify and remediate security risks related to sign-in risk policies 
	* Identify and remediate security risks related to Conditional Access events 
	* Identify and remediate security risks related to Azure Active Directory 
	* Identify and remediate security risks using Secure Score 
	* Identify, investigate, and remediate security risks related to privileged identities 
	* Configure detection alerts in Azure AD Identity Protection 
	* Identify and remediate security risks related to Active Directory Domain Services using Microsoft Defender for Identity 

* Detect, investigate, respond, and remediate application threats 
	* Identify, investigate, and remediate security risks by using Microsoft Cloud Application Security (MCAS) 
	* Configure MCAS to generate alerts and reports to detect threats

### Module 2

* Design and configure an Azure Defender implementation 
	* Plan and configure Azure Defender settings, including selecting target subscriptions and workspace 
	* Configure Azure Defender roles 
	* Configure data retention policies 
	* Assess and recommend cloud workload protection 

* Plan and implement the use of data connectors for ingestion of data sources in Azure Defender 
	* Identify data sources to be ingested for Azure Defender 
	* Configure Automated Onboarding for Azure resources 
	* Connect on-premises computers 
	* Connect AWS cloud resources 
	* Connect GCP cloud resources 
	* Configure data collection 

* Manage Azure Defender alert rules 
	* Validate alert configuration 
	* Setup email notifications 
	* Create and manage alert suppression rules

### Module 3 (Part 1)

* Design and configure an Azure Sentinel workspace 
	* Plan an Azure Sentinel workspace 
	* Configure Azure Sentinel roles 
	* Design Azure Sentinel data storage 
	* Configure Azure Sentinel service security 

* Plan and Implement the use of Data Connectors for Ingestion of Data Sources in Azure Sentinel 
	* Identify data sources to be ingested for Azure Sentinel 
	* Identify the prerequisites for a data connector 
	* Configure and use Azure Sentinel data connectors 
	* Configure data connectors by using Azure Policy 
	* Design and configure Syslog and CEF event collections 
	* Design and Configure Windows Events collections 
	* Configure custom threat intelligence connectors 
	* Create custom logs in Azure Log Analytics to store custom data 

* Manage Azure Sentinel analytics rules 
	* Design and configure analytics rules 
	* Create custom analytics rules to detect threats 
	* Activate Microsoft security analytical rules 
	* Configure connector provided scheduled queries 
	* Configure custom scheduled queries 
	* Define incident creation logic 

* Manage Azure Sentinel Incidents 
	* Investigate incidents in Azure Sentinel 
	* Triage incidents in Azure Sentinel 
	* Respond to incidents in Azure Sentinel 
	* Investigate multi-workspace incidents 
	* Identify advanced threats with User and Entity Behavior Analytics (UEBA) 

### Module 3 (Part 2)

* Configure Security Orchestration Automation and Response (SOAR) in Azure Sentinel 
	* Create Azure Sentinel playbooks 
	* Configure rules and incidents to trigger playbooks 
	* Use playbooks to remediate threats 
	* Use playbooks to manage incidents 
	* Use playbooks across Microsoft Defender solutions 

* Use Azure Sentinel workbooks to analyze and interpret data 
	* Activate and customize Azure Sentinel workbook templates 
	* Create custom workbooks 
	* Configure advanced visualizations 
	* View and analyze Azure Sentinel data using workbooks 
	* Track incident metrics using the security operations efficiency workbook 

* Hunt for threats using the Azure Sentinel portal 
	* Create custom hunting queries 
	* Run hunting queries manually 
	* Monitor hunting queries by using Livestream 
	* Perform advanced hunting with notebooks 
	* Track query results with bookmarks 
	* Use hunting bookmarks for data investigations 
	* Convert a hunting query to an analytic rule

### Exam Resources

* [Home page for the Exam](https://aka.ms/SC-200)
* [SC-200 offcial learning path](https://docs.microsoft.com/en-us/certifications/exams/sc-200)
* [In depth discussion of the exam concepts](https://aka.ms/YouTube/SC-200)
* [Study guide created by Charbel Nemnom, MVP](https://aka.ms/SC-200StudyGuide)

## Microsoft Identity and Access Administrator (SC-300)

### Exam Overview

* Implement an identity management solution (25-30%)
* Implement an authentication and access management solution (25-30%)
* Implement access management for apps (10-15%)
* Plan and implement an identity governance strategy (25-30%)

### Module 1

* Implement initial configuration of Azure Active Directory 
	* Configure and manage Azure AD directory roles 
	* Configure and manage custom domains 
	* Configure and manage device registration options 
	* Configure delegation by using administrative units 
	* Configure tenant-wide settings 

* Create, configure and manage identities 
	* Create, configure and manage users 
	* Create, configure and manage groups 
	* Manage licenses Implement and manage external identities 
	* Manage external collaboration settings in Azure Active Directory 
	* Invite external users (individually or in bulk) 
	* Manage external user accounts in Azure Active Directory 
	* Configure identity providers (social and SAML/WS-fed) 

* Implement and manage hybrid identity 
	* Implement and manage Azure Active Directory Connect (AADC) 
	* Implement and manage Azure AD Connect cloud sync 
	* Implement and manage Password Hash Synchronization (PHS) 
	* Implement and manage Pass-Through Authentication (PTA) 
	* Implement and manage seamless Single Sign-On (SSO) 
	* Implement and manage Federation (excluding manual ADFS deployments) 
	* Implement and manage Azure Active Directory Connect Health 
	* Troubleshoot synchronization errors

### Module 2

* Plan and implement Azure Multifactor Authentication (MFA) 
	* Plan Azure MFA deployment (excluding MFA Server) 
	* Implement and manage Azure MFA settings 
	* Manage MFA settings for users 

* Manage user authentication 
	* Administer authentication methods (FIDO2 / Passwordless) 
	* Implement an authentication solution based on Windows Hello for Business 
	* Configure and deploy self-service password reset 
	* Deploy and manage password protection 
	* Implement and manage tenant restrictions 

* Plan, implement and administer conditional access 
	* Plan and implement security defaults 
	* Plan conditional access policies 
	* Implement conditional access policy controls and assignments (targeting, applications, and conditions) 
	* Testing and troubleshooting conditional access policies 
	* Implement application controls 
	* Implement session management 
	* Configure smart lockout thresholds 

* Manage Azure AD Identity Protection 
	* Implement and manage a user risk policy 
	* Implement and manage sign-in risk policies 
	* Implement and manage MFA registration policy 
	* Monitor, investigate and remediate elevated risky users

### Module 3

* Plan, implement, and monitor the integration of Enterprise Apps for SSO 
	* Implement and configure consent settings 
	* Discover apps by using MCAS or ADFS app report 
	* Design and implement access management for apps 
	* Design and implement app management roles 
	* Monitor and audit access / Sign-Ons to Azure Active Directory integrated enterprise applications 
	* Integrate on-premises apps by using Azure AD application proxy 
	* Integrate custom saas apps for SSO 
	* Configure pre-integrated (gallery) saas apps 
	* Implement application user provisioning 

* Implement app registrations 
	* Plan your line of business application registration strategy 
	* Implement application registrations 
	* Configure application permissions 
	* Implement application authorization 
	* Plan and configure multi-tier application permissions

### Module 4

* Plan and implement entitlement management 
	* Define catalogs 
	* Define access packages 
	* Plan, implement and manage entitlements 
	* Implement and manage terms of use 
	* Manage the lifecycle of external users in Azure AD Identity Governance settings 

* Plan, implement and manage access reviews 
	* Plan for access reviews 
	* Create access reviews for groups and apps 
	* Monitor access review findings 
	* Manage licenses for access reviews 
	* Automate access review management tasks 
	* Configure recurring access reviews 

* Plan and implement privileged access 
	* Define a privileged access strategy for administrative users (resources, roles, approvals, thresholds) 
	* Configure Privileged Identity Management for Azure AD roles 
	* Configure Privileged Identity Management for Azure resources 
	* Assign roles ·
	* Manage PIM requests 
	* Analyze PIM audit history and reports 
	* Create and manage break-glass accounts 

* Monitor and maintain Azure Active Directory 
	* Analyze and investigate sign-in logs to troubleshoot access issues 
	* Review and monitor Azure AD audit logs 
	* Enable and integrate Azure AD diagnostic logs with Log Analytics / Azure Sentinel 
	* Export sign-in and audit logs to a third-party SIEM 
	* Review Azure AD activity by using Log Analytics / Azure Sentinel, excluding KQL use 
	* Analyze Azure Active Directory workbooks / reporting 
	* Configure notifications

### Exam Resources

* [Home page for the exam](https://aka.ms/SC-300)
* [SC-300 official learning plan](https://docs.microsoft.com/en-us/learn/paths/implement-identity-management-solution/)
* [In-depth discussion of the concepts](https://aka.ms/YouTube/SC-300)
* [Study guide from Charbel Nemnom, MVP](https://aka.ms/SC-300StudyGuide)
* [Exam Readiness tips and tricks](https://docs.microsoft.com/en-us/shows/exam-readiness-zone/?terms=sc-300)

## Microsoft Information Protection Administrator (SC-400) 

### Exam Overview

* Implement information protection (35-40%)
* Implement data loss prevention (30-35%)
* Implement information governance (25-30%)

### Module 1

*	Create and manage sensitive information types; use exact data match, fingerprinting and keyword dictionary
    *	Select a sensitive information type based on an organization's requirements
    *	Create and manage custom sensitive information types
    *	Create custom sensitive information types with exact data match
    *	Implement document fingerprinting 
    *	Create a keyword dictionary 

*	Create trainable classifiers, verify functionality and retrain the classifier to improve it
    *	Identify when to use trainable classifiers
    *	Create a trainable classifier
    *	Verify a trainable classifier is performing properly 
    *	Retrain a classifier

*	Sensitivity labels: create and configure labels; apply labels to Teams, SharePoint sites; publish labels using MCAS; monitor label usage with Activity and Content Explorer; use AIP unified label scanner
    *	Identify roles and permissions for administering sensitivity labels 
    *	Create sensitivity labels 
    *	Configure and manage sensitivity label policies 
    *	Apply sensitivity labels to Microsoft Teams, Microsoft 365 groups, and SharePoint sites 
    *	Configure and publish automatic labeling policies (excluding MCAS scenarios) 
    *	Monitor data classification and label usage by using label analytics tools such as content explorer and activity explorer 
    *	Apply bulk classification to on-premises data by using the AIP unified labelling scanner 
    *	Manage protection settings and marking for applied sensitivity labels 
    *	Apply protections and restrictions to email including content marking, usage, permission, encryption, expiration, etc. 

*	Configure encryption on email messages: use Office 365 Message Encryption or Advanced Message Encryption
    *	Define requirements for implementing Office 365 Message Encryption 
    *	Implement Office 365 Advanced Message Encryption

### Module 2

*	Create and configure data loss prevention policies 
    *	Recommend a data loss prevention solution for an organization 
    *	Configure data loss prevention for policy precedence 
    *	Configure policies for Microsoft Exchange email 
    *	Configure policies for Microsoft SharePoint sites 
    *	Configure policies for Microsoft OneDrive accounts 
    *	Configure policies for Microsoft Teams chat and channel messages 
    *	Integrate Microsoft Cloud App Security (MCAS) with Microsoft Information Protection 
    *	Configure policies in Microsoft Cloud App Security (MCAS) 
    *	Implement data loss prevention policies in test mode 

*	Implement and monitor Microsoft Endpoint data loss prevention 
      *	Configure policies for endpoints 
      *	Configure Endpoint data loss prevention settings 
      *	Recommend configurations that enable devices for Endpoint data loss prevention policies 
      *	Monitor endpoint activities 

*	Manage and monitor data loss prevention policies and activities 
    *	Manage and respond to data loss prevention policy violations 
    *	Review and analyze data loss prevention reports 
    *	Manage permissions for data loss prevention reports 
    *	Manage data loss prevention violations in Microsoft Cloud App Security (MCAS) 

### Module 3

*	Configure retention policies and labels 
    *	Create and apply retention labels 
    *	Create and apply retention label policies 
    *	Configure and publish auto-apply label policies 
    *	Manage data retention in Microsoft 365 
    *	Create and apply retention policies in Microsoft SharePoint and OneDrive 
    *	Create and apply retention policies in Microsoft Teams 
    *	Recover content in Microsoft Teams, SharePoint, and OneDrive 
    *	Recover content in Microsoft Exchange 
    *	Implement retention policies and tags in Microsoft Exchange 
    *	Apply mailbox holds in Microsoft Exchange 
    *	Implement Microsoft Exchange Online archiving policies 
  
*	Implement records management in Microsoft 365 
    *	Configure labels for records management 
    *	Manage and migrate retention requirements with a file plan 
    *	Configure automatic retention using File Plan descriptors 
    *	Classify records using retention labels and policies 
    *	Implement in-place records management in Microsoft SharePoint 
    *	Configure event-based retention 
    *	Manage disposition of record
  
### Exam Resources
  
* [Home page for the exam](https://aka.ms/SC-400)
* [SC-400 official learning plan](https://docs.microsoft.com/en-us/learn/paths/implement-data-loss-prevention/)
* [In-depth discussion of the exam concepts](https://aka.ms/YouTube/SC-400)
* [Study guide created by Charbel Nemnom MVP](https://charbelnemnom.com/sc-400-exam-study-guide-microsoft-information-protection-administrator/)
* [SC 400 Learning  Path for Partners](https://partner.microsoft.com/en-us/training/assets/collection/microsoft-information-protection-administrator-sc-400#/)
* [Microsoft Certification Live Training for Partners](https://partner.microsoft.com/en-us/marketing/cloud-weeks)
