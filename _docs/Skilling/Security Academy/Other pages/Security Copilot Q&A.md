---
layout: page
title: Copilot for Security Q&A
description: Common Copilot for Security Q&A.
permalink: /skilling/microsoft-security-academy/microsoft-copilot-for-security-qa
updated: 2024-08-30
showbreadcrumb: true
tags: 
- academy content
- microsoft security academy
- security copilot
---

# Copilot for Security Q&A

#### Can my MSSP manage Copilot for Security on my behalf?
MSSPs can access customer tenants through both Guest Access (B2B) and Granular Delegated Admin Permissions (GDAP). Customers are responsible for purchasing their own Security Compute Units (SCUs) and configuring MSSP access in alignment with these permissions.

#### Can I use a single instance of Copilot for Security to manage multiple tenants?
Currently, Copilot for Security does not support cross-tenant prompting. However, MSSPs can utilize Tenant Switching to focus on ***one customer tenant at a time.*** MSSPs can choose the specific customer tenant from a dropdown menu within the in-product UX. Additionally, they have the option to include the TenantID (GUID) in the Copilot for Security session URL. Multi-Workspace and Multi-Tenancy (e.g., Azure Lighthouse) support ***are coming soon.***

#### Does Copilot for Security have a "token limit"?
LLMs like GPT have a "token limit" that restricts data processing. Copilot for Security uses the latest GPT models to process as much data as possible, but large prompts or long sessions may exceed this limit. When this happens, Copilot tries to provide an output, but if it fails, you may need to try a different prompt or plugin.

#### What is the Microsoft Copilot Copyright Commitment?
The Microsoft Customer Copyright Commitment extends intellectual property indemnity support to specific commercial Copilot services, including Copilot for Security. If a 3rd-party sues a commercial customer for copyright infringement related to the use of Microsoft’s Copilots or their generated output, Microsoft will defend the customer and cover any adverse judgments or settlements resulting from the lawsuit, provided that the customer adhered to the guardrails and content filters within the products.

#### Is my data protected?
ChatGPT was trained on data from the Internet. Copilot for Security does not leverage ChatGPT, or any data not owned by the customer and/or by Microsoft. In simpler terms, Copilot for Security **does not use your data to train foundation AI models.**

Additionally, **Copilot for Security does not share your data with OpenAI.**

#### Can we trust AI?
Copilot for Security is built with our **[Responsible AI principles](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1%3aprimaryr6).** Additionally, Copilot for Security uses Role-based access controls (RBAC) and operates in tandem with existing user permissions.

#### How is access and authorization governed?
Copilot for Security uses on-behalf-of (OBO) authentication to access security-related data through plugins. As such, the user will only be presented with data that they have access to. To access the Copilot for Security portal, users must be assigned a Microsoft Entra RBAC role (either directly or through a group) that has access to a given feature. Learn more about OAuth 2.0 On-Behalf-Of authentication **[here](https://learn.microsoft.com/en-us/entra/identity-platform/v2-oauth2-on-behalf-of-flow)** and overall authentication in Copilot for Security **[here](https://learn.microsoft.com/en-us/security-copilot/authentication).**

#### How can I measure success?
Consider defining some use case scenarios (e.g., writing reports/summaries) and estimate the time to fulfill the task with and without Copilot for Security. Discuss use cases based on who is able to lead them and whether they can assign more junior analysts more senior tasks. Lastly, and thanks to Copilot for Security's efficiency, determine if your team is able to manage more proactive security tasks.

#### Will Copilot for Security "hallucinate"?
To ensure the accuracy of Copilot for Security's responses, Microsoft's Threat Intelligence (TI) data, model fine-tuning, and the user's connected skillsets ground Copilot for Security to prevent hallucinations. Copilot for Security also outlines the steps and sources it uses to arrive at an answer, allowing users to verify the results provided.

If a user is dissatisfied with Copilot for Security's response, they have the option to provide feedback within the platform. Feedback is encouraged and contributes to the ongoing improvement of response quality.

#### What is a "planner" or "orchestrator"?
An orchestrator is an autonomous agent in an environment that is tasked to achieve a goal by deciding action(s). The state of the agent gets updated after each action execution. Given an NL question from the user, the orchestrator (1) Understands the intent using an LLM (2) Generates a Plan (3) Executes the Plan (4) Prepares the response for the user (5) Preserves and updates the state (Ex: memory, chat history).

#### Will Copilot for Security take remediation action?
Copilot for Security cannot perform remediation actions on your behalf, but there is potential for more automation in the future.

#### How can I build effective prompts?
Learn to create effective, natural language inputs (prompts) in Copilot for Security **[here](https://learn.microsoft.com/en-us/security-copilot/prompting-tips).**

#### Can I build my own Copilot for Security plugins?
Learn how to develop your own custom plugins **[here](https://learn.microsoft.com/en-us/security-copilot/manage-plugins?tabs=securitycopilotplugin#custom-plugins).**

#### Does Copilot for Security work in US Government Cloud (GCC)?
As of now, Copilot for Security does not support US Government clouds, including but not limited to GCC, GCC High, DoD, and Microsoft Azure Government.

#### Does Copilot for Security support customers under HIPAA regulations?
Copilot for Security does support US customers who are subject to regulations under HIPAA.

#### Does Copilot for Security support any other Compliance Offerings?
Copilot for Security supports ISO27001, 27018, 27017, 27701, 20000-1, 9000-1and 22301.