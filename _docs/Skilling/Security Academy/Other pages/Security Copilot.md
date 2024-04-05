---
layout: page
title: Copilot for Security
description: Are you ready for Copilot for Security?
permalink: /skilling/microsoft-security-academy/microsoft-copilot-for-security
updated: 2024-04-04
showbreadcrumb: true
tags: 
- academy content
- microsoft security academy
- security copilot
---

# Copilot for Security Technical Resources

## What is Copilot for Security? 🤔

Microsoft Copilot for Security is the first security product to enable defenders to move at the speed and scale of AI. It combines the most advanced large language models (LLMs) from OpenAI with large-scale data and threat intelligence, including more than 78 trillion daily security signals.

## April 5th, 2024 Update📰

Copilot for Security is globally available as of April-1! Despite the April Fools' Day launch, we're serious about Copilot for Security's GA and transformative power. With all the recent developments, my colleague Sameh Younis and I are planning significant updates to this page. Stay tuned.

It's been two days since GA and we're receiving some questions about why Copilot for Security is automatically appearing in Defender XDR. Since Copilot for Security uses Role-based access controls (RBAC) and operates in tandem with existing user permissions, if you belong to an RBAC group with access, you will not be able to disable it.

We're aware of this issue and a fix should come soon. If you're new to Copilot for Security or just getting started, I’ve added some **[onboarding guidance](/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#onboarding)** below.

I was in Redmond two weeks ago presenting Copilot for Security at the Microsoft AI Cloud Summit. The attendees, most of whom had surprisingly never seen it, were fascinated. Leaving the conference, it's apparent most partners are confused about the pricing. Below, I added details about Copilot for Security's **[newly-released pricing](/PartnerResources/skilling/microsoft-security-academy/microsoft-copilot-for-security#pricing).**

Whether you're new to Copilot for Security or in the [Microsoft Copilot for Security Partner Ecosystem](https://securitypartners.transform.microsoft.com/copilot-private-preview-partners), expand your capabilities with our [Copilot for Security documentation](https://learn.microsoft.com/en-us/security-copilot/).

[Prompt engineering in Copilot for Security](https://learn.microsoft.com/en-us/security-copilot/prompting-tips) plays a critical role in creating specific, high-quality outputs. **[This folder](https://github.com/rod-trent/Security-Copilot/tree/main/Prompts)** contains Copilot for Security prompting templates and Promptbooks.

## Events

* [**Learn Live:** Get started with Microsoft Copilot for Security (March 19-April 9)](https://learn.microsoft.com/en-us/shows/learn-live/microsoft-copilot-for-security/) -- this is a "can't miss" event
* [**Microsoft Copilot for Security Partner Boot Camp** (April 16-17)](https://vshow.on24.com/vshow/FY24_SDepth/registration/23173)

## Secure Update🔓

Read [Vasu Jakkal's Copilot for Security April-1 global availability announcement](https://www.microsoft.com/en-us/security/blog/2024/03/13/microsoft-copilot-for-security-is-generally-available-on-april-1-2024-with-new-capabilities/). Copilot for Security has grown into an ecosystem of more than [100 partners](https://securitypartners.transform.microsoft.com/copilot-private-preview-partners)! As the ecosystem continues to grow, so too will **[Non-Microsoft plugins](https://learn.microsoft.com/en-us/security-copilot/plugin-other).** As a partner, learn how to create and manage your own custom plugins **[here](https://learn.microsoft.com/en-us/security-copilot/manage-plugins?tabs=securitycopilotplugin).**

Also, explore the results of our recent **[Randomized Controlled Trial for Copilot for Security](https://go.microsoft.com/fwlink/?linkid=2262764&clcid=0x409&culture=en-us&country=us).**

## Get Started

To get started, we recommend watching the following videos created by Microsoft Security and the Global Partner Solutions (GPS) Technical Team:

<table>
  <tr style="vertical-align:top">
   <td><a href="https://youtu.be/0lg_derTkaM?si=qrp0F_GcPwFPoI7i"><img src="https://img.youtube.com/vi/0lg_derTkaM/maxresdefault.jpg" alt="How Microsoft Copilot for Security works" width="300" height="250"></a></td>
    <td><a href="https://youtu.be/0lg_derTkaM?si=qrp0F_GcPwFPoI7i"><b>How Microsoft Copilot for Security works</b></a><br><br>Ryan Munsch, from the Copilot for Security team, joins host Jeremy Chapman to share how Copilot for Security is an enterprise-grade natural language interface for your organization's security data.</td>
  </tr>
  <tr style="vertical-align:top">
   <td><a href="https://www.youtube.com/watch?v=dNvdeJA6m4g"><img src="https://img.youtube.com/vi/dNvdeJA6m4g/maxresdefault.jpg" alt="Prepare for New Threats with Microsoft Copilot for Security" width="300" height="250"></a></td>
    <td><a href="https://www.youtube.com/watch?v=dNvdeJA6m4g"><b>Prepare for New Threats with Microsoft Copilot for Security</b></a><br><br>Join Dave and Zach as they discuss how to prepare for new threats in an era of increasingly complex cyberattacks with Microsoft Copilot for Security. Explore Copilot for Security’s interface, how a partner gains access, the power of plugins and Promptbooks, data security and privacy, AI threats and how we at Microsoft defeat them, and our Responsible AI story.</td>
  </tr>
  <tr style="vertical-align:top">
   <td><a href="https://youtu.be/2mL9iDr_lUY?si=ePBzuIBQT8In-zz8"><img src="https://img.youtube.com/vi/2mL9iDr_lUY/maxresdefault.jpg" alt="Microsoft Copilot for Security & Tanium Demo" width="300" height="250"></a></td>
    <td><a href="https://youtu.be/2mL9iDr_lUY?si=lWO3C49hAFIPrhqs"><b>Microsoft Copilot for Security & Tanium Demo</b></a><br><br>Tanium introduces their Copilot for Security proof of concept to enable responses in minutes with real-time visibility.</td>
  </tr>
</table>

## Pricing📌

Copilot for Security pricing is consumption-based and costs approximately **$4 per SCU per hr.** A **Security Compute Unit (SCU)** is Copilot for Security's unit of measurement of computing capacity to run Copilot workloads. The amount of SCUs needed depends on the complexity of the workload. The pricing is consistent across the standalone experience and the embedded experiences as well all regions.

Why is it consumption-based and not per user? The idea is that the flexibility will allow more customers and partners to try it! That said, the output is only as good as the input, and the more plugins you may use to contextually enrich complex investigations, the better (think Microsoft Sentinel pricing; the more telemetry ingested = the more coverage and insights, so long as it's not *too* much noise). There are no prerequisites, but for the best experience, we recommend that customers have MDE P2 and/or Microsoft Sentinel.

To use Copilot for Security, you will need to provision ***at least* one SCU per hr 24x7.** Therefore, the **minimum annual price is $35,040 USD** ($4 * 24hr per day * 365day per yr). Your *monthly* bill is calculated as (SCUs per hr) x $4 x 730/month and you can leverage the [Azure Pricing Calculator](https://azure.microsoft.com/en-us/pricing/calculator/) to estimate your monthly cost. Customers and partners can purchase SCUs in the standalone experience or in Azure and can manually provision SCUs up or down so long as there is ***at least* one SCU/hr.** Once an analyst is nearing the capacity limit, they will receive a warning and the option to increase the capacity.

If you delete Copilot for Security capacity (zero SCUs per hr), we will retain your data for 90 days. **Tenant-level MDTI workbench is included** and while it's not the standalone API, the TI information is easy to read and in the context of your investigations. From a licensing perspective, this is also **significant cost savings.**

Since computing capacity and token usage is **variable (quantifying a specific # of tokens or SCUs/workflows needed per prompt/Promptbook is difficult)**, it's important for partners to know what they can do *now:*

* Measure SCU usage between different use cases (SOC analysts, Purview admins, identity/access admins, etc.)
* Measure SCU usage between different levels of expertise (Junior analysts vs Senior analysts)
* Measure SCU usage across different types of investigations (incident triage, threat actor investigation, reverse engineering a malicious script, etc.)

I'm assuming beyond the EAP, we're also collecting this data and in good time, will provide more guidance and standards on SCU usage patterns and what ***is and isn't a SCU/workflow.***

## Onboarding

You can provision Copilot for Security within the [standalone experience](https://learn.microsoft.com/en-us/security-copilot/get-started-security-copilot#option-1-recommended-provision-capacity-through-copilot-for-security) or in [Azure](https://learn.microsoft.com/en-us/security-copilot/get-started-security-copilot#option-2-provision-capacity-in-azure). If your organization requires tags to deploy Azure resources, use **[this ARM template](https://github.com/seanstark/azure-tools/tree/main/copilotforsecurity)** to add tags during deployment. When provisioning Copilot for Security, you can purchase capacity in these four regions: East US, West Europe, UK South, and Australia East.

While there are technically no prerequisites, you'll need an Azure subscription and Microsoft Entra ID (Entra ID is required to authenticate your users). We also recommend allowing prompt evaluation anywhere with available GPU capacity for optimal results. By default, ***all users are contributors*** (this may vary according to existing user permissions) and ***the provisioning user is the owner.*** Contributors cannot update data sharing options, manage SCUs, view the usage dashboard, and may only manage and publish custom plugins or upload files when allowed.

I recommend starting with Promptbooks. You can easily add tags, edit, share, run, and set the level of access to "Just me" or "Anyone in my organization." You can even create your own. Learn more about how to create your own Promptbooks **[here](https://learn.microsoft.com/en-us/security-copilot/build-promptbooks).** It's also critical to monitor SCU usage to manage costs and avoid disruptions. Learn more about how to monitor your usage **[here](https://learn.microsoft.com/en-us/security-copilot/manage-usage).** Also, if you’re beginning with the embedded experiences, I recommend ***starting with Defender XDR.***

Lastly, experiment with uploading your organizations own DOCX, MD, PDF, and TXT files. You can upload files up to 20 MB in total. Copilot for Security reasons over files to generate more relevant and specific responses. Learn more about uploading your own files **[here](https://learn.microsoft.com/en-us/security-copilot/upload-file).**

## Features

* Incident Response — Summarize incidents, assess impact, and receive tailored remediation guidance, including for triage, investigation, and containment.
* Security Reports — Summarize investigations, incidents, vulnerabilities, or threats in minutes and prepare the information in ready-to-share reports.
* Security Posture Management — Learn if your organization is at risk from vulnerabilities and examine resources in your environment for signs of a breach.
* Reverse Script Engineering — Analyze complex command line scripts and translate them into natural language with clear explanations of actions.

## Roles beyond SOC Analysts​

* **DLP​ Analysts:​** Summarize DLP alerts and analyze DLP policy configurations.
* **Insider​ Risk Analysts:​** Summarize Insider Risk Management alerts and gain context around users with risky behavior​.
* **IT​ Admins:** Create device configuration profiles in Intune and leverage data-driven configuration troubleshooting and remediation​.
* **eDiscovery​ Analysts​:** Generate Keyword Query Language from NL in eDiscovery and summarize evidence collected.
* **Identity Access Management​ Admins:** Discover high risk users, overprivileged access, suspicious sign-ins in Entra.

## Demos

* [Business Email Compromise (BEC)](https://securitypartners.transform.microsoft.com/copilot-for-security-demo-01)
* [Human-operated ransomware (HumOR)](https://securitypartners.transform.microsoft.com/copilot-for-security-demo-02)
* [Defender XDR Embedded Copilot to Standalone Copilot investigation](https://securitypartners.transform.microsoft.com/copilot-for-security-demo-03)
* [Extended user account investigation](https://securitypartners.transform.microsoft.com/copilot-for-security-demo-04)
* [Cloud compromise](https://securitypartners.transform.microsoft.com/copilot-for-security-demo-05)
* [Troubleshooting](https://securitypartners.transform.microsoft.com/copilot-for-security-demo-06)

## Integrations

* [Microsoft Copilot for Security in Microsoft Defender XDR](https://learn.microsoft.com/en-us/microsoft-365/security/defender/security-copilot-in-microsoft-365-defender?view=o365-worldwide&bc=%2Fsecurity-copilot%2Fbreadcrumb%2Ftoc.json&toc=%2Fsecurity-copilot%2Ftoc.json)
* [Microsoft Copilot for Security in Microsoft Entra](https://learn.microsoft.com/en-us/entra/fundamentals/copilot-security-entra?bc=%2Fsecurity-copilot%2Fbreadcrumb%2Ftoc.json&toc=%2Fsecurity-copilot%2Ftoc.json)
* [Microsoft Copilot for Security and Intune](https://learn.microsoft.com/en-us/mem/intune/fundamentals/security-copilot?bc=%2Fsecurity-copilot%2Fbreadcrumb%2Ftoc.json&toc=%2Fsecurity-copilot%2Ftoc.json)
* [Microsoft Copilot for Security and Defender EASM](https://learn.microsoft.com/en-us/azure/external-attack-surface-management/easm-copilot?bc=%2Fsecurity-copilot%2Fbreadcrumb%2Ftoc.json&toc=%2Fsecurity-copilot%2Ftoc.json)
* [Microsoft Copilot for Security and Microsoft Defender Threat Intelligence](https://learn.microsoft.com/en-us/defender/threat-intelligence/security-copilot-and-defender-threat-intelligence?bc=%2Fsecurity-copilot%2Fbreadcrumb%2Ftoc.json&toc=%2Fsecurity-copilot%2Ftoc.json)
* [Microsoft Copilot for Security in Microsoft Purview](https://learn.microsoft.com/en-us/purview/copilot-in-purview-overview?bc=%2Fsecurity-copilot%2Fbreadcrumb%2Ftoc.json&toc=%2Fsecurity-copilot%2Ftoc.json)

## Architecture (updated)


![MSA Organizational Chart]({{ site.baseurl }}/assets/msa/CfS Arch.png)


#### Considerations

* **Assist a Human in Completing Work** – It's a Copilot, integrations are driven by/drive human engagement, not background runtime processing of substantial amounts of data.
* **Have High Customer Value** — The cost of Generative AI is orders of magnitude higher per transaction than your average feature today and depends on a constrained hardware supply (GPUs).
* **Will be Regularly Used** — The best integrations will be used regularly so it is ongoing value, not a one-time value (like a configuration assistant).

#### How does Copilot for Security increase efficiency?

-> *[Reference](https://techcommunity.microsoft.com/t5/microsoft-security-copilot-blog/improving-threat-hunting-efficiency-using-copilot-for-security/ba-p/4077527?utm_source=substack&utm_medium=email)*

* **Threat Hunting:** Assists in building hunting queries by reasoning over MDTI.
* **Speed:** Improves security teams’ response time, with up to a [26% reduction in randomized control trials.](https://www.microsoft.com/en-us/security/blog/2023/12/06/microsoft-security-copilot-drives-new-product-integrations-at-microsoft-ignite-to-empower-security-and-it-teams/)
* **Efficiency:** Enhances responses with contextual summaries, reduces routine tasks, and offers Natural Language to KQL conversion (NL2KQL).
* **More Proactive Threat Hunting:** Empowers teams with AI-powered recommendations.
* **Empowering Staff:** Frees senior staff for strategic work and strengthens junior staff expertise.

## AI Security
* Learn more about our approach to **[Responsible AI](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1%3aprimaryr6).**
* **[Apply principles of Zero Trust to Microsoft Copilot for Security](https://learn.microsoft.com/en-us/security/zero-trust/copilots/zero-trust-microsoft-copilot-for-security)**
* **[MITRE ATLAS (Adversarial Threat Landscape for Artificial-Intelligence Systems)](https://atlas.mitre.org/?utm_source=substack&utm_medium=email)**
* [Must Learn AI Security](https://github.com/rod-trent/OpenAISecurity/tree/main/Must_Learn)
* [OWASP AI Security and Privacy Guide](https://owasp.org/www-project-ai-security-and-privacy-guide/)
* [Introduction to red teaming large language models (LLMs)](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/red-teaming?utm_source=substack&utm_medium=email)

## Community Resources
* [Microsoft Copilot for Security Blog](https://techcommunity.microsoft.com/t5/microsoft-security-copilot-blog/bg-p/SecurityCopilotBlog)
* [OpenAI's GPT Best Practices](https://platform.openai.com/docs/guides/gpt-best-practices)

## Interesting Reads
* [Why AI Will Save the World](https://a16z.com/2023/06/06/ai-will-save-the-world/?utm_source=substack&amp;utm_medium=email)
* [Microsoft AI Red Team Building a Future of Safer AI](https://www.microsoft.com/en-us/security/blog/2023/08/07/microsoft-ai-red-team-building-future-of-safer-ai/?utm_source=substack&utm_medium=email)
