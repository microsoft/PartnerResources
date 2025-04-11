---
layout: page
title: Security Copilot
description: Security Copilot Technical Journey
permalink: /skilling/microsoft-security-academy/microsoft-copilot-for-security
updated: 2025-04-11
showbreadcrumb: true
tags: 
- academy content
- microsoft security academy
- security copilot
---

# Security Copilot Resources

## What is the Security Copilot Technical Journey? <img src="https://raw.githubusercontent.com/Azure/Copilot-For-Security/main/Images/ic_fluent_copilot_64_64%402x.png" alt="CfS Logo" style="width: 35px; height: auto;">

The Microsoft Security Copilot Technical Journey will guide you through how to learn, extend, and drive customer adoption for Microsoft Security Copilot, the first security platform to enable defenders to move at the speed and scale of AI by leveraging the most advanced large language models (LLMs) with large-scale data and threat intelligence, including more than 78 trillion daily security signals.

## Table of Contents

This page is organized into three parts -- Learn, Extend, and Driving Adoption.


<table>
    <tr>
        <td colspan="2" style="text-align: center;"><b>Table of Contents</b></td>
    </tr>
    <tr>
        <td><b><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#learn-copilot-for-security">Learn Security Copilot</a></b></td>
        <td>
            <ul>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#overview">Overview</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#onboarding">Onboarding</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#get-started">Get Started</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#use-cases">Use Cases</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#videos">Videos</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#roles-beyond-soc-analysts">Roles</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#announcements--whitepapers">Announcements & Whitepapers</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#community-resources">Community Resources</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#ai-security">AI Security</a></li>
            </ul>
        </td>
    </tr>
    <tr>
        <td><b><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#extend-copilot-for-security">Extend Security Copilot</a></b></td>
        <td>
            <ul>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#mssps">Granting an MSSP access</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#plugins">Plugins</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#connectors">Connectors</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#3p-plugins">3P Plugins</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#extensibility-features">Extensibility Features</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#community-plugins">Community Plugins</a></li>
            </ul>
        </td>
    </tr>
    <tr>
        <td><b><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#driving-customer-adoption">Driving Customer Adoption</a></b></td>
        <td>
            <ul>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#pricing">Pricing</a></li>     
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#integrations">Integrations</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#microsoft-security-integration-reference-architecture">Microsoft Security Integration Reference Architecture</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#multi-tenant--delegation-models">Multi-tenant & Delegation Models</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#address-concerns">Address Concerns</a></li>
                <li><a href="/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#technical-considerations">Technical Considerations</a></li>
            </ul> 
        </td>
    </tr>
</table>

___

## April 11th, 2025 Update📰

**Recent Update** (April 11th): **[Events](/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#events)** and **[Get Started](/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#get-started)** |

We *finally* published **[official documentation](https://learn.microsoft.com/en-us/copilot/security/plugin-splunk?utm_source=substack&utm_medium=email)** on the Splunk plugin in Security Copilot📌

MSSPs, this one’s for you: **[Security Copilot support for Azure Lighthouse is now in public preview](https://techcommunity.microsoft.com/blog/SecurityCopilotBlog/azure-lighthouse-support-for-mssp-use-of-security-copilot-sentinel-scenarios-in-/4384386?utm_source=substack&utm_medium=email)**

If you've been waiting to use Security Copilot with your managed customers, good news: support is here (well, *mostly*). So, what's the catch? As of today, MSSPs can ***only invoke Sentinel skills*** on their customer tenants via the ***Security Copilot standalone portal.*** In the future, this will expand to include other skills such as Entra, Intune, Purview, and the list goes on. What's changed? Customers are no longer required to ***purchase the SCUs themselves.***

To get started...

1. An MSSP admin should provision SCUs (including the new **[Overage SCUs](https://learn.microsoft.com/en-us/copilot/security/manage-usage#how-provisioned-and-overage-scus-are-billed)**, which are $6 per SCU/hour and billed only on usage), and apply them to your Azure Lighthouse subscription
2. Make sure you have access to your customer’s Sentinel workspace


Just last week, we announced **[Security Copilot agents](https://www.microsoft.com/en-us/security/blog/2025/03/24/microsoft-unveils-microsoft-security-copilot-agents-and-new-protections-for-ai/?msockid=330c4da567d667543ffd5c5666b966cf)** that automate repetitive, noisy tasks like user-reported phishing alerts, conditional access policy gaps for new users and apps, and DLP/IRM alerts.

Think of these agents ***more like advanced workflows*** or simplified Logic Apps — automated, *mostly* trigger-based sequences for specific tasks + you can guide them with feedback/custom instructions in natural language. Most won’t take action for you, but they'll help you prioritize (e.g., classifying phish alerts as true or false positive, one-click fixes for users outside existing MFA policies, ...)

Who doesn't want to make incident response in Sentinel faster and smarter? **[This new post](https://www.linkedin.com/pulse/incident-enrichment-security-copilot-stefano-pescosolido-hldcf/)** walks through how you can use Security Copilot with Logic Apps and MDTI to automatically enrich incidents, cut down triage time, and get better insights.

Security Copilot egress IPs are **[now published](https://learn.microsoft.com/en-us/copilot/security/plugin-ip-address?utm_source=substack&utm_medium=email)** to help you send requests and receive responses from your plugins!


### Older news

You can learn how to access the Security Copilot audit log **[here](https://learn.microsoft.com/en-us/copilot/security/audit-log)** or how you can ingest your Security Copilot audit logs using **[this Azure Function App and PowerShell script](https://github.com/Azure/Security-Copilot/tree/main/Monitoring/IngestSecurityCopilotAuditlogs).**

It's also worth exploring **[this solution](https://github.com/Azure/Security-Copilot/tree/main/Logic%20Apps/SecCopilot-UserReportedPhishing-FuncApp_parsing)**  that automates the analysis of user-submitted phishing emails using Security Copilot🎣

Lastly, my colleague Rick created **[these easy-to-use KQL templates](https://github.com/Azure/Security-Copilot/blob/main/Plugins/MSFT_Plugin_Samples/KQL/KQL_Combined_Defender_and_Sentinel_Example.yaml)** for custom Defender and Sentinel plugins. Give them a try!


### Events

If you're a member of the **[Microsoft Security Copilot Customer Connection Program (CCP)](http://www.aka.ms/prseccom)**, join our weekly Security Copilot Skilling and Readiness events:

| **Topic** | **Date & Time** | **Register!** |
|  AMA with the Security Copilot in Entra team           | Tuesday, April 15th @  8:00 AM PT | [Register](https://msit.events.teams.microsoft.com/event/929cde16-e6a2-4913-b28b-d0fdcf467260@72f988bf-86f1-41af-91ab-2d7cd011db47)
|  New capabilities announced at Microsoft Secure        | Thursday, April 17th @  8:00 AM PT | [Register](https://msit.events.teams.microsoft.com/event/f7b6361f-12f7-42aa-a663-a4659bdd8798@72f988bf-86f1-41af-91ab-2d7cd011db47)
|  Conditional Access Optimization Agent in Entra        | Thursday, May 1st @  8:00 AM PT | [Register](https://msit.events.teams.microsoft.com/event/55f93283-dc1b-4326-bd73-2a700fdff50a@72f988bf-86f1-41af-91ab-2d7cd011db47)
|  Splunk plugin for Security Copilot                    | Thursday, May 8th @  8:00 AM PT | [Register](https://msit.events.teams.microsoft.com/event/caeb0bcb-9165-41bc-b2d5-064f2e64b18a@72f988bf-86f1-41af-91ab-2d7cd011db47)


<div>&nbsp;</div>

___


## Learn Security Copilot

Are you ready to get started? Dive into onboarding guidance, prompt engineering templates and best practices, community resources, and other relevant documentation.

### Overview

* [What is Microsoft Security Copilot?](https://learn.microsoft.com/en-us/security-copilot/microsoft-security-copilot?view=o365-worldwide)
* [Microsoft Security Copilot experiences](https://learn.microsoft.com/en-us/security-copilot/experiences-security-copilot?view=o365-worldwide)
* [Navigate Security Copilot](https://learn.microsoft.com/en-us/security-copilot/navigating-security-copilot?view=o365-worldwide)
* [Create effective prompts](https://learn.microsoft.com/en-us/security-copilot/prompting-tips?view=o365-worldwide)
* [What is a compound AI system?](https://bair.berkeley.edu/blog/2024/02/18/compound-ai-systems/)
* [Using Microsoft Graph as a Microsoft Security Copilot Plugin with Delegated Access](https://techcommunity.microsoft.com/t5/microsoft-security-copilot-blog/using-microsoft-graph-as-a-microsoft-copilot-for-security-plugin/ba-p/4198148)

### Onboarding

You can provision Security Copilot within the [standalone experience](https://learn.microsoft.com/en-us/security-copilot/get-started-security-copilot#option-1-recommended-provision-capacity-through-copilot-for-security) or in [Azure](https://learn.microsoft.com/en-us/security-copilot/get-started-security-copilot#option-2-provision-capacity-in-azure). If your organization requires tags to deploy Azure resources, use **[this ARM template](https://github.com/seanstark/azure-tools/tree/main/copilotforsecurity)** to add tags during deployment. When provisioning Security Copilot, you can purchase capacity in these **four regions:** East US, West Europe, UK South, and Australia East. Customers can provision a maximum of 100 SCUs and scale down to a minimum of 1 SCU per hr.

While there are technically no prerequisites, you'll need an Azure subscription and Microsoft Entra ID (Entra ID is required to authenticate your users). We also recommend allowing prompt evaluation anywhere with available GPU capacity for optimal results. By default, ***all users are "Copilot contributors"*** (this may vary according to existing user permissions) and ***the provisioning user is the "Copilot owner."*** Contributors cannot update data sharing options, manage SCUs, view the usage dashboard, and may only manage and publish custom plugins or upload files when allowed. Also by default, ***all security administrators and global administrators inherit Security Copilot access.***

Security Copilot will **not** elevate your level of access (e.g., to use the Microsoft Sentinel plugin, you will need the Microsoft Sentinel Reader role). However, plugin settings are managed at the ***user level***, requiring each user to enable/disable plugins and configure authentication methods. Unfortunately, there is no existing option to set plugin configurations at the ***Tenant level.***

I recommend starting with the Defender XDR Embedded Experience or Promptbooks. You can easily add tags, edit, share, run, and set the level of access to "Just me" or "Anyone in my organization." You can even create your own. Learn more about how to create your own Promptbooks **[here](https://learn.microsoft.com/en-us/security-copilot/build-promptbooks).** It's also critical to monitor SCU usage to manage costs and avoid disruptions (e.g., calculate your average SCU utilization over a standard 7 days). Learn more about how to monitor your usage **[here](https://learn.microsoft.com/en-us/security-copilot/manage-usage).** Microsoft permits ***some occasional demand spikes*** from customers that exceed their provisioned capacity at no additional charge, but if the spikes are consistent, that usually signals under provisioned capacity.

Lastly, experiment with uploading your organizations own DOCX, MD, PDF, and TXT files. You can upload files up to 20 MB in total. Security Copilot reasons over files to generate more relevant and specific responses. Learn more about uploading your own files **[here](https://learn.microsoft.com/en-us/security-copilot/upload-file).**

---

We recommend provisioning Security Copilot from the **Azure Portal** rather than the standalone experience, since issues like resource tagging or location policies tend to show up more clearly there. Also, by default, users with the Entra **Global Admin** or **Security Admin** roles will automatically be assigned the **Security Copilot Owner** role.

And one more tip: it’s a good idea to start with a small number of SCUs and focus first on the embedded experiences—they’re much more stable and less likely to run into setup snags.

This is a great step forward for MSSPs looking to bring AI-driven security to their customers. Check out the full blog post to dive deeper and take your next steps today!

### Get Started

* [Get started](https://learn.microsoft.com/en-us/security-copilot/get-started-security-copilot?view=o365-worldwide)
* [Understand authentication](https://learn.microsoft.com/en-us/security-copilot/authentication?view=o365-worldwide)
* [Best practices for Microsoft Entra roles](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/best-practices#1-apply-principle-of-least-privilege)
* [Prompting](https://learn.microsoft.com/en-us/security-copilot/prompting-security-copilot?view=o365-worldwide)
* [Promptbooks](https://learn.microsoft.com/en-us/security-copilot/using-promptbooks?view=o365-worldwide)
* **NEW:** [Prompt Engineering Techniques: A comprehensive repository](https://github.com/NirDiamant/Prompt_Engineering)
* [OpenAI Prompt Engineering](https://platform.openai.com/docs/guides/gpt-best-practices)
* [Apply principles of Zero Trust to Microsoft Security Copilot](https://learn.microsoft.com/en-us/security/zero-trust/copilots/zero-trust-microsoft-copilot-for-security)
* [Exploring Security Copilot to Automate Incident Triage](https://techcommunity.microsoft.com/t5/microsoft-security-copilot-blog/exploring-copilot-for-security-to-automate-incident-triage/ba-p/4154887)

#### Optional resources for after your first few months

##### **Useful for analysts**

* [Next-Gen device incident investigation and threat hunting with custom plugins](https://techcommunity.microsoft.com/blog/securitycopilotblog/next-gen-device-incident-investigation--threat-hunting-with-custom-plugins/4374397?utm_source=substack&utm_medium=email)
* [Accelerating anomalous sign-in detection with Security Copilot + Entra ID](https://techcommunity.microsoft.com/blog/securitycopilotblog/accelerating-the-anomalous-sign-ins-detection-with-microsoft-entra-id-and-securi/4365435?utm_source=substack&utm_medium=email)
* [Monitoring user activities and system events with Security Copilot + Sentinel](https://techcommunity.microsoft.com/blog/securitycopilotblog/monitor-user-activities-and-system-events-with-security-copilot-and-microsoft-se/4303368?utm_source=substack&utm_medium=email)

##### **Useful for customization**

* [Leveraging ASIM-based KQL plugins in Security Copilot](https://techcommunity.microsoft.com/blog/securitycopilotblog/leveraging-asim-based-kql-plugins-in-microsoft-security-copilot-for-investigatio/4357680?utm_source=substack&utm_medium=email)
* [Custom Identity Analyst plugin](https://techcommunity.microsoft.com/blog/securitycopilotblog/identity-forensics-with-copilot-for-security-identity-analyst-plugin/4278180)
* [Custom Data Security plugin](https://techcommunity.microsoft.com/t5/security-compliance-and-identity/learn-how-to-customize-and-optimize-copilot-for-security-with/ba-p/4120147?utm_source=substack&utm_medium=email)

##### **Useful for extension**

* [Extending Security Copilot with Azure Function Apps](https://techcommunity.microsoft.com/t5/microsoft-security-copilot-blog/extending-microsoft-copilot-for-security-capabilities-with-azure/ba-p/4220267?utm_source=substack&utm_medium=email)

### Use Cases

* [Triage incidents with enriched threat intelligence](https://learn.microsoft.com/en-us/security-copilot/triage-alert-with-enriched-threat-intel?view=o365-worldwide)
* [Investigate an incident's malicious script](https://learn.microsoft.com/en-us/security-copilot/investigate-incident-malicious-script?view=o365-worldwide)
* [Advanced Hunting](https://learn.microsoft.com/en-us/microsoft-365/security/defender/advanced-hunting-security-copilot?view=o365-worldwide)
* [Summarize an incident in Microsoft Defender XDR](https://learn.microsoft.com/en-us/microsoft-365/security/defender/security-copilot-m365d-incident-summary?view=o365-worldwide)
* [Use guided responses in Defender XDR](https://learn.microsoft.com/en-us/microsoft-365/security/defender/security-copilot-m365d-guided-response?view=o365-worldwide)
* [Create an incident report in Microsoft Defender XDR](https://learn.microsoft.com/en-us/microsoft-365/security/defender/security-copilot-m365d-create-incident-report?view=o365-worldwide)
* [Script analysis in Defender XDR](https://learn.microsoft.com/en-us/microsoft-365/security/defender/security-copilot-m365d-script-analysis?view=o365-worldwide)
* [Generate device summaries in Defender XDR](https://learn.microsoft.com/en-us/microsoft-365/security/defender/copilot-in-defender-device-summary?view=o365-worldwide)
* [Analyze files in Defender XDR](https://learn.microsoft.com/en-us/microsoft-365/security/defender/copilot-in-defender-file-analysis?view=o365-worldwide)
* [Risky user summarization in Entra](https://learn.microsoft.com/en-us/entra/fundamentals/copilot-entra-risky-user-summarization)
* [Summarize the latest threats in MDTI](https://learn.microsoft.com/en-us/defender/threat-intelligence/using-copilot-threat-intelligence-defender-xdr#prioritize-which-threats-to-focus-on)
* [Analyze recommendations in MDC](https://learn.microsoft.com/en-us/azure/defender-for-cloud/analyze-with-copilot)
* [Summarize recommendations in MDC](https://learn.microsoft.com/en-us/azure/defender-for-cloud/summarize-with-copilot)
* [Remediate recommendations in MDC](https://learn.microsoft.com/en-us/azure/defender-for-cloud/remediate-with-copilot)
* [Delegate recommendations in MDC](https://learn.microsoft.com/en-us/azure/defender-for-cloud/delegate-with-copilot)
* [Remediate code in MDC](https://learn.microsoft.com/en-us/azure/defender-for-cloud/remediate-code-with-copilot)

### Videos

We recommend watching the following videos created by Microsoft Security and the Global Partner Solutions (GPS) Technical Team:

<table>
  <tr style="vertical-align:top">
   <td><a href="https://youtu.be/7hNbYOjh-1k?si=hTiYUf628nR4aC4A"><img src="https://img.youtube.com/vi/7hNbYOjh-1k/maxresdefault.jpg" alt="Microsoft Security Copilot" width="400" height="400"></a></td>
    <td><a href="https://youtu.be/7hNbYOjh-1k?si=hTiYUf628nR4aC4A"><b>Microsoft Security Copilot</b></a><br><br>John Savill dives into the powerful features and capabilities of Microsoft Security Copilot.</td>
  </tr>
  <tr style="vertical-align:top">
   <td><a href="https://youtu.be/rm2-C49fXBM"><img src="https://img.youtube.com/vi/rm2-C49fXBM/maxresdefault.jpg" alt="Threat Intelligence in Security Copilot with Volt/Silk Typhoon demo" width="400" height="400"></a></td>
    <td><a href="https://youtu.be/rm2-C49fXBM"><b>Threat Intelligence in Security Copilot with Volt/Silk Typhoon demo</b></a><br><br>Learn about Microsoft Threat Intelligence in Security Copilot, including what it is, how you can use it, and learn from a comprehensive demo featuring Volt/Silk Typhoon, prolific state-sponsored espionage actors from China.</td>
  </tr>
  <tr style="vertical-align:top">
   <td><a href="https://youtu.be/EZrKUtxFnGU?si=dWxf3UePboDB8tKU"><img src="https://img.youtube.com/vi/EZrKUtxFnGU/maxresdefault.jpg" alt="Security Copilot Pricing" width="400" height="400"></a></td>
    <td><a href="https://youtu.be/EZrKUtxFnGU?si=dWxf3UePboDB8tKU"><b>Security Copilot Pricing</b></a><br><br>Short on time? Learn about Security Copilot’s pricing model in just 10 minutes, including how to provision, scale, and manage Security Compute Units (SCUs). Discover what you can do today, along with valuable onboarding tips.</td>
  </tr>
  <tr style="vertical-align:top">
   <td><a href="https://youtu.be/AxO8iduHoNA?si=NnzWOMTXhCGvvD7_"><img src="https://img.youtube.com/vi/AxO8iduHoNA/maxresdefault.jpg" alt="Selling Security Copilot w/ Multi-stage Incident Demo" width="400" height="400"></a></td>
    <td><a href="https://youtu.be/AxO8iduHoNA?si=NnzWOMTXhCGvvD7_"><b>Selling Security Copilot w/ Multi-stage Incident Demo</b></a><br><br>Explore Security Copilot’s powerful use cases, its unique value, proven results, and differentiation story, and see it all in action with a comprehensive multi-stage incident demo in Microsoft Defender XDR.</td>
  </tr>
  <tr style="vertical-align:top">
   <td><a href="https://youtu.be/DSL-nPWUXlY?si=NSQvyGyhMakPGLZX"><img src="https://img.youtube.com/vi/DSL-nPWUXlY/maxresdefault.jpg" alt="Security Copilot Responsible AI
" width="400" height="400"></a></td>
    <td><a href="https://youtu.be/DSL-nPWUXlY?si=NSQvyGyhMakPGLZX"><b>Security Copilot Responsible AI</b></a><br><br>Learn how Security Copilot mitigates Responsible AI issues and explore Generative AI threats, including prompt injection attacks, disinformation campaigns, spear phishing, etc., and how we at Microsoft defeat them.</td>
  </tr>
</table>

#### Also explore [Microsoft's Security Copilot YouTube Playlist](https://youtube.com/playlist?list=PL3ZTgFEc7LyuQRLD61q9YqPKEDlZj4j5u&si=uAY93F-cGoZNPXPP)📹

### Roles beyond SOC Analysts​

* **IT​ Admins:** Create device configuration profiles in Intune and leverage data-driven configuration troubleshooting and remediation​.
* **DLP​ Analysts:​** Summarize DLP alerts and analyze DLP policy configurations.
* **Insider​ Risk Analysts:​** Summarize Insider Risk Management (IRM) alerts and gain context around users with risky behavior​.
* **eDiscovery​ Analysts​:** Generate Keyword Query Language from NL in eDiscovery and summarize evidence collected.
* **Identity Access Management (IAM)​ Admins:** Discover high risk users, overprivileged access, and users out of compliance.
* **CISOs:** Receive executive summaries and detailed reporting.

### Announcements & Whitepapers

* **Nov. 2024:** [Generative AI and SOC Productivity: Evidence from Live Operations](https://cdn-dynmedia-1.microsoft.com/is/content/microsoftcorp/microsoft/final/en-us/microsoft-brand/documents/Generative-AI-and-Security-Operations-Center-Productivity-Evidence-from-Live-Operations_v2.5-FINAL.pdf)
* **Oct. 2024:** [Randomized Controlled Trials for Security Copilot for IT Admins](https://arxiv.org/html/2411.01067v1)

### Community Resources

* [Join the Security Copilot Customer Connection Program (CCP)](http://www.aka.ms/prseccom)
* [Microsoft Security Copilot Tech Community Blog](https://techcommunity.microsoft.com/t5/microsoft-security-copilot-blog/bg-p/SecurityCopilotBlog)
* [Applied Generative AI (GAI) in Security Blog](https://applied-gai-in-security.ghost.io/)
* [Why AI Will Save the World Blog](https://a16z.com/2023/06/06/ai-will-save-the-world/?utm_source=substack&amp;utm_medium=email)

### AI Security

* Learn more about our approach to [Responsible AI](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1%3aprimaryr6)
* [MITRE ATLAS (Adversarial Threat Landscape for Artificial-Intelligence Systems)](https://atlas.mitre.org/matrices/ATLAS)
* [OWASP AI Security and Privacy Guide](https://owasp.org/www-project-ai-security-and-privacy-guide/)


#### [Back to Table of Contents](/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#table-of-contents). Are you ready to extend Security Copilot?


<div>&nbsp;</div>

___


## Extend Security Copilot

Learn how to grant an MSSP access and how to use and create plugins. Security Copilot plugins extend the platform’s capabilities by acting as connectors, enabling seamless integration with infinite partners and third parties, allowing for custom functionality.

### MSSPs

* [Grant MSSP access](https://learn.microsoft.com/en-us/security-copilot/grant-access-external-users?view=o365-worldwide)

### Plugins

As of today, custom plugins in Security Copilot work by executing ***1. a KQL query, 2. a GPT query, or 3. making an API call*** (either GET or POST), and the data returned depends on the type of call and the associated API permissions.

* [Overview](https://learn.microsoft.com/en-us/security-copilot/plugin-overview?view=o365-worldwide)
* [Other plugins](https://learn.microsoft.com/en-us/copilot/security/plugin-other) -- ***Non-Microsoft plugins***
* [API](https://learn.microsoft.com/en-us/security-copilot/plugin-api?view=o365-worldwide)
* [GPT](https://learn.microsoft.com/en-us/security-copilot/plugin-gpt?view=o365-worldwide)
* [KQL](https://learn.microsoft.com/en-us/security-copilot/plugin-kql?view=o365-worldwide)
* [Manage plugins](https://learn.microsoft.com/en-us/security-copilot/manage-plugins?view=o365-worldwide&tabs=securitycopilotplugin)
* [Create custom plugins](https://learn.microsoft.com/en-us/copilot/security/custom-plugins?view=o365-worldwide)
* [Plugin error codes](https://learn.microsoft.com/en-us/security-copilot/plugin-error-codes?view=o365-worldwide)

### Connectors

* [Overview](https://learn.microsoft.com/en-us/connectors/securitycopilot/)
* [Logic Apps](https://learn.microsoft.com/en-us/security-copilot/connector-logicapp?view=o365-worldwide)
* [Logic Apps error codes](https://learn.microsoft.com/en-us/copilot/security/logic-apps-error-codes?view=o365-worldwide)
* [Logic Apps Templates](https://github.com/Azure/Copilot-For-Security/tree/main/Logic%20Apps)

### 3P Plugins

* [AbuseIPDB](https://learn.microsoft.com/en-us/copilot/security/plugin-abuseipdb) -- AbuseIPDB is a central repository to report and identify IPs that are associated with malicious activity online
* [Aviatrix](https://learn.microsoft.com/en-us/copilot/security/plugin-aviatrix) -- Aviatrix provides insights into cloud networking and firewall policy enforcement
* [CheckPhish](https://learn.microsoft.com/en-us/copilot/security/plugin-checkphish) --  CheckPhish AI analyzes URLs for phishing threats, tech support scams, cryptojacking, and other risks
* [Computer Incident Response Center Luxembourg (CIRCL)](https://learn.microsoft.com/en-us/copilot/security/plugin-circl) -- CIRCL is a government initiative to validate suspicious files in the form of hashes
* [CrowdSec](https://learn.microsoft.com/en-us/copilot/security/plugin-crowdsec) -- CrowdSec provides identification and verification of potentially malicious IPs
* [CyberArk](https://learn.microsoft.com/en-us/copilot/security/plugin-cyberark) -- CyberArk Privilege Cloud helps to securely store, rotate, and isolate credentials
* [Cybersixgill](https://learn.microsoft.com/en-us/copilot/security/plugin-cybersixgill) -- Cybersixgill offers real-time TI solutions, including from the dark web
* [Cyware Intel Exchange](https://learn.microsoft.com/en-us/copilot/security/plugin-cyware-intel-exchange) -- Cyware Intel is a TI Platform for ingestion, enrichment, analysis, prioritization, actioning, and sharing of threat data
* [Cyware Respond](https://learn.microsoft.com/en-us/copilot/security/plugin-cyware) -- Cyware Respond is an end-to-end incident management and response platform
* [Darktrace](https://learn.microsoft.com/en-us/copilot/security/plugin-darktrace) -- Darktrace offers cybersecurity AI services
* [Forescout Risk and Exposure Management](https://learn.microsoft.com/en-us/copilot/security/plugin-forescout-rem) -- Forescout REM provides a view of device risks and vulnerabilities
* [Forescout Vedere Labs](https://learn.microsoft.com/en-us/copilot/security/plugin-forescout-vedere-labs) -- Forescout research teams provide a TI feed containing IP, URL, and File hash indicators for potentially malicious activity
* [GreyNoise](https://learn.microsoft.com/en-us/copilot/security/plugin-greynoise) -- GreyNoise collects and analyzes Internet-wide scan and attack data
* [Intel 471](https://learn.microsoft.com/en-us/copilot/security/plugin-intel471) -- Intel 471 provides cybercrime intelligence
* [IPGeolocation](https://learn.microsoft.com/en-us/copilot/security/plugin-ipgeolocation) -- IPGeolocation provides geolocation data, time zone details, security insights (VPN, proxy, bot detection), etc.
* [IPinfo](https://learn.microsoft.com/en-us/copilot/security/plugin-ipinfo) -- IPinfo provides IP geolocation, IP to Privacy Detection (VPN, Tor, Proxy), ASN data, company data, carrier metadata, and WHOIS data
* [Jamf](https://learn.microsoft.com/en-us/copilot/security/plugin-jamf) -- Jamf Pro provides enterprise-level Mobile Device Management (MDM)
* [Netskope](https://learn.microsoft.com/en-us/copilot/security/plugin-netskope) -- Netskope combines security and networking services, enabling Secure Access Services Edge (SASE) and Zero Trust
* [Pure Signal Scout](https://learn.microsoft.com/en-us/copilot/security/plugin-pure-signal-scout) -- Pure Signal Scout is Team Cymru's TI tool
* [Quest Security Guardian](https://learn.microsoft.com/en-us/copilot/security/plugin-quest-security-guardian) -- Quest Security Guardian is an Active Directory tool that reduces your attack surface
* [Red Canary](https://learn.microsoft.com/en-us/copilot/security/plugin-red-canary) -- Red Canary provides managed detection and response (MDR) services
* [ReversingLabs](https://learn.microsoft.com/en-us/copilot/security/plugin-reversinglabs) -- ReversingLabs helps SOC teams understand file-based threats
* [Saviynt](https://learn.microsoft.com/en-us/copilot/security/plugin-saviynt) -- Saviynt provides insights into identity-related risks
* [SGNL](https://learn.microsoft.com/en-us/copilot/security/plugin-sgnl) -- SGNL provides Zero Standing Privilege (ZSP) initiatives to protect user sessions and credentials
* [Shodan](https://learn.microsoft.com/en-us/copilot/security/plugin-shodan) -- Shodan is a search engine that allows users to find specific types of devices connected to the Internet
* [Silverfort](https://learn.microsoft.com/en-us/copilot/security/plugin-silverfort) -- Silverfort provides advanced CEF data from Microsoft Sentinel
* **NEW:** [Splunk!](https://learn.microsoft.com/en-us/copilot/security/plugin-splunk) -- Splunk is a widely used SIEM, SOAR, and threat intelligence platform
* [Tanium](https://learn.microsoft.com/en-us/copilot/security/plugin-tanium) -- Tanium is a Converged Endpoint Management (XEM) reference platform
* [TufinMate](https://learn.microsoft.com/en-us/copilot/security/plugin-tufinmate) -- Tufin Orchestration Suite is a firewall management platform
* [UrlScan](https://learn.microsoft.com/en-us/copilot/security/plugin-urlscan) -- UrlScan allows users to scan and analyze potentially malicious URLs
* [Valence Security](https://learn.microsoft.com/en-us/copilot/security/plugin-valence) -- Valence combines SaaS Security Posture Management (SSPM) and advanced remediation
* [Whoisfreaks](https://learn.microsoft.com/en-us/copilot/security/plugin-whoisfreaks) -- Whoisfreaks provides domain and IP intelligence services

### Extensibility Features

![CfS Reference Architecture]({{ site.baseurl }}/assets/msa/CfS Extensibility.jpg)

### Relevant Community Plugins

**Disclaimer:** ***Some of these plugins were developed and are maintained by the community and are not owned and/or managed by Microsoft.***

* [Security Copilot Login Activities](https://github.com/Azure/Copilot-For-Security/tree/main/Plugins/Community%20Based%20Plugins/Copilot%20Logins)
* [Microsoft Sentinel custom plugin scenarios](https://github.com/Azure/Copilot-For-Security/tree/main/Plugins/Community%20Based%20Plugins/Microsoft%20Sentinel%20Custom%20Plugin%20Scenarios)
* [Microsoft Defender XDR custom plugin scenarios](https://github.com/Azure/Copilot-For-Security/tree/main/Plugins/Community%20Based%20Plugins/Microsoft%20Defender%20XDR%20Custom%20Plugin%20Scenarios)
* [QR Code AiTM Phishing Detection](https://github.com/Azure/Copilot-For-Security/tree/main/Plugins/Community%20Based%20Plugins/QR%20Code%20AiTM%20Phishing%20Detection%20Plugin)
* [Redact Personally Identifiable Information (PII)](https://github.com/Azure/Copilot-For-Security/tree/main/Plugins/Community%20Based%20Plugins/HaveIBeenPwned) -- this plugin will redact PII content from a session or a prompt ouput
* [Have I Been Pwned](https://github.com/Azure/Copilot-For-Security/tree/main/Plugins/Community%20Based%20Plugins/HaveIBeenPwned) -- Have I Been Pwned allows users to verify whether their personal data has been compromised by data breaches


#### [Back to Table of Contents](/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#table-of-contents). Are you ready to drive customer adoption?


<div>&nbsp;</div>

___


## Driving Customer Adoption

Microsoft Security Copilot enables customers and partners to defend against threats, streamline security workflows, and protect critical assets. Learn how to drive customer adoption below.

### Pricing📌

Security Copilot pricing is consumption-based and costs approximately **$4 per SCU per hr.** A Security Compute Unit (SCU) is Security Copilot's unit of measurement of computing capacity to run a Copilot workload (i.e., prompt/Promptbook). The amount of SCUs needed depends on the complexity of the given workload. The pricing is consistent across the standalone experience and the embedded experiences as well as regions.

Why is it consumption-based and not per user? The idea is that the flexibility will allow more customers and partners to try it! That said, the output is only as good as the input, and the more plugins you use to contextually enrich complex investigations, the better (think Microsoft Sentinel pricing; the more telemetry ingested = the more coverage and insights, so long as it's not *too* much noise). There are no prerequisites, but for the optimal user experience, we recommend that customers have MDE P2 and/or Microsoft Sentinel.

To use Security Copilot, you will need to provision ***at least* 1 SCU per hr 24x7.** Therefore, the ***minimum annual price is $35,040 USD*** ($4 * 24hr per day * 365day per yr). Your ***monthly*** bill is calculated as (SCUs per hr) x $4 x 730/month or you can leverage the [Azure Pricing Calculator](https://azure.microsoft.com/en-us/pricing/calculator/). Customers and partners can purchase SCUs in the standalone experience or in Azure and can manually provision SCUs up or down so long as there is ***at least* 1 SCU/hr.** Once an analyst is nearing the capacity limit (90%), they will receive a warning and the option to increase the capacity.

If you delete Security Copilot (zero SCUs per hr), we will retain your data for 90 days. ***Tenant-level MDTI workbench is included with Security Copilot*** and although it's not the standalone API, the TI information is easy to read and in the context of your investigations (e.g., activity groups, tooling, and vulnerabilities). From a licensing perspective, this is also **significant cost savings.**

Since computing capacity and token usage is ***variable*** **(quantifying a specific # of tokens or SCUs/workflows needed per prompt/Promptbook is difficult)**, it's important for partners to know what they can do now:

* Calculate your average SCU utilization over a standard 7 days
* Provision ≈1 SCU per Embedded Experience, ≈4 SCU per Standalone Experience, and ≈5 SCU per Automation and/or Promptbooks
* Measure SCU usage between different use cases (SOC analysts, Purview admins, Identity/access admins, etc.)
* Measure SCU usage between different levels of expertise (Junior analysts vs Senior analysts)
* Measure SCU usage across different types of investigations (incident triage, threat actor investigation, reverse engineering a malicious script, etc.)
* Explore the **[Security Copilot SCU Optimizer Solution](https://locktalk.substack.com/p/introducing-the-copilot-for-security?r=3eb8k1&utm_campaign=post&utm_medium=web&triedRedirect=true)** to simplify CfS cost management

Beyond GA, we're also collecting this data and in good time, will provide more guidance and standards on SCU usage and patterns.

### Integrations

* [Microsoft Security Copilot in Microsoft Defender XDR](https://learn.microsoft.com/en-us/microsoft-365/security/defender/security-copilot-in-microsoft-365-defender?view=o365-worldwide&bc=%2Fsecurity-copilot%2Fbreadcrumb%2Ftoc.json&toc=%2Fsecurity-copilot%2Ftoc.json)
* [Microsoft Security Copilot in Microsoft Entra](https://learn.microsoft.com/en-us/entra/fundamentals/copilot-security-entra?bc=%2Fsecurity-copilot%2Fbreadcrumb%2Ftoc.json&toc=%2Fsecurity-copilot%2Ftoc.json)
* [Microsoft Security Copilot and Intune](https://learn.microsoft.com/en-us/mem/intune/fundamentals/security-copilot?bc=%2Fsecurity-copilot%2Fbreadcrumb%2Ftoc.json&toc=%2Fsecurity-copilot%2Ftoc.json)
* [Microsoft Security Copilot and Defender EASM](https://learn.microsoft.com/en-us/azure/external-attack-surface-management/easm-copilot?bc=%2Fsecurity-copilot%2Fbreadcrumb%2Ftoc.json&toc=%2Fsecurity-copilot%2Ftoc.json)
* [Microsoft Security Copilot and Microsoft Threat Intelligence](https://learn.microsoft.com/en-us/defender/threat-intelligence/security-copilot-and-defender-threat-intelligence?bc=%2Fsecurity-copilot%2Fbreadcrumb%2Ftoc.json&toc=%2Fsecurity-copilot%2Ftoc.json)
* [Microsoft Security Copilot in Microsoft Purview](https://learn.microsoft.com/en-us/purview/copilot-in-purview-overview?bc=%2Fsecurity-copilot%2Fbreadcrumb%2Ftoc.json&toc=%2Fsecurity-copilot%2Ftoc.json)
* [Security Copilot in Defender for Cloud (Preview)](https://learn.microsoft.com/en-us/azure/defender-for-cloud/copilot-security-in-defender-for-cloud?bc=%2Fsecurity-copilot%2Fbreadcrumb%2Ftoc.json&toc=%2Fsecurity-copilot%2Ftoc.json&view=o365-worldwiden)


### Microsoft Security Integration Reference Architecture

![CfS Reference Architecture]({{ site.baseurl }}/assets/msa/CfS Reference Arch.jpg)

### Multi-tenant & Delegation Models

As of today, MSSPs can ***only invoke Sentinel skills*** on their customer tenants via the ***Security Copilot standalone portal.*** Support for other skills like Entra, Intune, and Purview is coming soon. What's changed? Customers are no longer required to ***purchase the SCUs themselves.***

To get started, an MSSP admin should 1. provision SCUs (including the new **[Overage SCUs](https://learn.microsoft.com/en-us/copilot/security/manage-usage#how-provisioned-and-overage-scus-are-billed)**, which are $6 per SCU/hour and billed only on usage) and 2. apply them to their Azure Lighthouse subscription. Then, 3. make sure you have access to your customer’s Sentinel workspace.

* [Azure Lighthouse](https://techcommunity.microsoft.com/blog/SecurityCopilotBlog/azure-lighthouse-support-for-mssp-use-of-security-copilot-sentinel-scenarios-in-/4384386?utm_source=substack&utm_medium=email)
* [Grant partners access](https://learn.microsoft.com/en-us/security-copilot/grant-access-external-users?view=o365-worldwide)
* [B2B collaboration](https://learn.microsoft.com/en-us/entra/external-id/what-is-b2b)
* [Granular Delegated Admin Privileges (GDAP)](https://learn.microsoft.com/en-us/partner-center/gdap-introduction)

### Address Concerns

* [OAuth 2.0 On-Behalf-Of flow](https://learn.microsoft.com/en-us/entra/identity-platform/v2-oauth2-on-behalf-of-flow)
* [Privileged Identity Management (PIM)](https://learn.microsoft.com/en-us/entra/id-governance/privileged-identity-management/)
* [Microsoft Defender for Endpoint (MDE) Device Groups](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/machine-groups?view=o365-worldwide)

### Technical Considerations

* **Assist a Human in Completing Work** – It's a Copilot, integrations are driven by/drive human engagement, not background runtime processing of large amounts of data.
* **Have High Customer Value** — The cost of Generative AI is orders of magnitude higher per transaction than your average feature today and depends on a constrained hardware supply (GPUs).
* **Will be Regularly Used** — The best integrations will be used regularly so it is ongoing value, not a one-time value (like a configuration assistant).


#### [Back to Table of Contents](/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#table-of-contents).