---
layout: page
title: Copilot for Security Q&A
description: Common Copilot for Security Q&A.
permalink: /skilling/microsoft-security-academy/microsoft-security-copilot-extra
updated: 2024-02-20
showbreadcrumb: true
tags: 
- academy content
- microsoft security academy
- security copilot
---

# Copilot for Security Q&A

#### Is my data protected?
ChatGPT was trained on data from the Internet. Copilot for Security does not leverage ChatGPT, or any data not owned by the customer and/or by Microsoft. In simpler terms, Copilot for Security **does not use your data to train foundation AI models.**

Additionally, **Copilot for Security does not share your data with OpenAI.**

#### Can we trust AI?
Copilot for Security is built with our **[responsible AI principles](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1%3aprimaryr6).** Additionally, Copilot for Security uses Role-based access controls (RBAC) and operates in tandem with existing user permissions.

#### How is access and authorization governed?
Copilot for Security uses on-behalf-of (OBO) authentication to access security-related data through plugins. As such, the user will only be presented with data that they have access to. To access the Copilot for Security portal, users must be assigned a Microsoft Entra RBAC role (either directly or through a group) that has access to a given feature.

#### Will Copilot for Security "hallucinate"?
To ensure the accuracy of Copilot for Security's responses, Microsoft's Threat Intelligence (TI) data, model fine-tuning, and the user's connected skillsets ground Copilot for Security to prevent hallucinations. Copilot for Security also outlines the steps and sources it uses to arrive at an answer, allowing users to verify the results provided.

If a user is dissatisfied with Copilot for Security's response, they have the option to provide feedback within the platform. Feedback is encouraged and contributes to the ongoing improvement of response quality.

#### How can I measure success?

Consider defining some use case scenarios (e.g., writing reports/summaries) and estimate the time to fulfill the task with and without Copilot for Security. Discuss use cases based on who is able to lead them and whether they can assign more junior analysts more senior tasks. Lastly, and thanks to Copilot for Security's efficiency, determine if your team is able to manage more proactive security tasks.

#### What is a "planner" or "orchestrator"?
An orchestrator is an autonomous agent in an environment that is tasked to achieve a goal by deciding action(s). The state of the agent gets updated after each action execution. Given an NL question from the user, the orchestrator (1) Understands the intent using an LLM (2) Generates a Plan (3) Executes the Plan (4) Prepares the response for the user (5) Preserves and updates the state (Ex: memory, chat history).

#### Can I build my own Copilot for Security plugins?
Learn how to develop your own custom plugins **[here](https://learn.microsoft.com/en-us/security-copilot/manage-plugins?tabs=securitycopilotplugin#custom-plugins).**

#### How can I build effective prompts?
Learn to create effective, natural language inputs (prompts) in Copilot for Security **[here](https://learn.microsoft.com/en-us/security-copilot/prompting-tips).**

#### How is Copilot for Security different from competitor solutions?
There is no comparative to Copilot for Security. Picture a scenario in which a junior analyst uses natural language to access incident data from Sentinel, compare that data with alerts from Defender, gain insights into potentially impacted devices through Intune, and receive threat intelligence flags for known threat actors, all within **one platform.** This junior analyst can also easily share the investigation with colleagues and automatically generate incident reports. Competitor solutions are also limited to their 1st party ecosystem.