---
layout: page
title: AI & ML Academy - Agentic AI
sorttitle: 02
description: Agentic AI
permalink: /skilling/ai-ml-academy/agenticAI
updated: 2024-04-04
showbreadcrumb: true
tags: 
- azure
- data, analytics, and ai
- artificial intelligence
- machine learning
- academy content
- ai & ml academy module
- ai & ml academy
- AI agents
---

# AI & ML Academy - Agentic AI

Welcome to the AI & ML Academy (AIA) – Agentic AI!

This section includes an Agentic AI overview, architecture examples, end-to-end scenarios, demos, and other QuickStart resources.
Also explore our [Azure OpenAI resources page](📖)

## Agentic AI Overview

### 1. What are Agents?
Agents are AI designed to perform a task – these tasks can vary in level of complexity and capabilities depending on your need. At the simplest level, agents can retrieve information from grounding data, reason, and answer user questions. At the most advanced level, autonomous agents can operate independently, orchestrating other agents, learn and plan. Agents are comprised of key components including Knowledge, Models, and Actions, as well as Orchestrators, Memory, and Autonomy, all wrapped within a User Experience.

- **User Experience**: The prompt that starts the whole process of the agent execution, as well as the human-agent interaction.
- **Knowledge**: Search and retrieve information from online sources or company knowledge base, to ground the models
- **Actions**: Helps the agents perform certain actions (e.g. send an email, write a report) through connections to key applications.
- **Memory and Threads**: Captures and stores the past interactions for hyper-personalisation and increased human-like interactions
- **Autonomy**: Leaves the agents perform the tasks through an event-driven, trigger-based approach
- **Foundation Models**: Enables AI Agents to think throughout the process, helping to plan and reflect.
- **Orchestrators**: Whether to be the client-side code or orchestrate across multiple agents across multiple clouds, orchestrators are key to bringing everything together.

### 2. Use Cases
Key use cases across industries include personalized customer support, employee onboarding, data analytics and reporting, and travel booking and expense management:

### 3. Choosing the Right Approach for Your Requirements
Choosing the right tool and approach to build your agent depends on your skillset, customization, and control requirements.

For end users building agents via natural language, M365 Copilot empowers users to build agents based on Microsoft Graph or documents in SharePoint or Public Websites. Users can build powerful retrieval agents which help answer user questions.

Copilot Studio enables makers to build powerful agents using Low-code. These agents can connect to various sources like Graph connectors, Custom Connectors (API based), Dataverse, SharePoint documents, Public websites and more. Agents built using Copilot Studio can not only retrieve information, but can also take action on the user’s behalf. Makers can also create autonomous agents which will function independently of user interaction.

Lastly, AI Foundry empowers developers to build agents from a pro-code approach, offering the highest level, of agent complexity and customization.

### 4. Getting Started With Agents
This guide walks through getting started in a zero-to-hour format for building agents leveraging Azure AI Agent Service, Semantic Kernel, and AutoGen. For a self-paced Cloud Skills Learning Collection, please see GPS Americas - Agentic AI Self Paced Challenge.

| Lesson | Text & Code | Video | Extra Learning |
|--------|--------------|-------|----------------|
| Intro to AI Agents and Agent Use Cases | [Link](Link) | [Video](Video) | [Link](Link) |
| Exploring AI Agentic Frameworks | [Link](Link) | [Video](Video) | [Link](Link) |
| Understanding AI Agentic Design Patterns | [Link](Link) | [Video](Video) | [Link](Link) |
| Tool Use Design Pattern | [Link](Link) | [Video](Video) | [Link](Link) |
| Agentic RAG | [Link](Link) | [Video](Video) | [Link](Link) |
| Building Trustworthy AI Agents | [Link](Link) | [Video](Video) | [Link](Link) |
| Planning Design Pattern | [Link](Link) | [Video](Video) | [Link](Link) |
| Multi-Agent Design Pattern | [Link](Link) | [Video](Video) | [Link](Link) |
| Metacognition Design Pattern | [Link](Link) | [Video](Video) | [Link](Link) |
| AI Agents in Production | [Link](Link) | [Video](Video) | [Link](Link) |

## Best Practices for Agent Design
You’ll find that Microsoft’s AI stack — including Azure and Copilot Studio — offers everything you need to build robust, agentic AI frameworks. It’s a comprehensive and well-integrated platform that supports rapid development, scalability, and secure deployment. That said, many clients do choose a multi-cloud strategy, and it’s absolutely possible to design agentic solutions that interoperate across platforms like AWS, GCP, and OCP.

While portability can vary depending on architecture and dependencies, adopting open standards, containerization, and modular design patterns makes it easier to build agents that aren’t tightly coupled to a single provider. So, while you don’t need to compromise on capabilities within Azure, maintaining flexibility is entirely feasible if multi-cloud resilience is a priority for your organization.

To learn more about leveraging MCP within Microsoft’s Agentic AI ecosystem, please see Introducing Model Context Protocol (MCP) in Azure AI Foundry: Create an MCP Server with Azure AI Agent Service and Introducing Model Context Protocol (MCP) in Copilot Studio: Simplified Integration with AI Apps and Agents.

## Key Build Announcements
The following strategic announcements were announced at Build 2025:

## Demo-ready Resources
Below is a table of Accelerators and workshops that can be leveraged for pro-code Agentic AI demos.

| Demo | Framework/Approach | Aligned Industry |
|------|---------------------|------------------|
| [GitHub - shivachittamuru/langgraph-agents-on-azure: Build and deploy production-grade langgraph agents on Azure using Chinook database](LangGraph) | Agnostic/Retail |
| [GitHub - Azure-Samples/azure-ai-agent-service-enterprise-demo: Demonstrates how to build a streaming enterprise agent using Azure AI Agent Service. This sample integrates local HR and company policy documents, Bing for external context, and GPT-4o](Azure AI Agent Service) | HR/Internal |
| [GitHub - microsoft/ai-agents-for-beginners: 10 Lessons to Get Started Building AI Agents](Azure AI Agent Service) | Semantic Kernel Autogen Agnostic |
| [GitHub - Azure-Samples/agent-openai-java-banking-assistant: multi-agents banking assistant with Java and Semantic Kernel](Semantic Kernel) | FSI |
| [GitHub - Azure-Samples/multi-agent-workshop: A short set of exercises that showcase the usage of autogen to create agents](Autogen 0.4) | Agnostic |
| [GitHub - Azure-Samples/dream-team: This repo helps you to build a team of AI agents with Autogen](Autogen 0.4) | Retail/FSI/Oil+Gas |
| [GitHub - Azure-Samples/azure-sql-db-chat-sk at insurance-chatbot-demo](Semantic Kernel) | Insurance |
| [GitHub - Azure-Samples/azure-postgresql-openai-langchain-autogen-demo: Multi-Agent AI System with LangChain, AutoGen, Azure OpenAI GPT-4, and Azure PostgreSQL](Autogen) | Retail/Manufacturing |

## End-to-end Solutions
A collection of solution accelerators (repositories) that show you how to create a robust, end-to-end Agentic AI solution.

| Name | Application | Description |
|------|-------------|--------------|
| [GitHub - Azure-Samples/azure-ai-agent-service-enterprise-demo: Demonstrates how to build a streaming enterprise agent using Azure AI Agent Service. This sample integrates local HR and company policy documents, Bing for external context, and GPT-4o](Azure AI Agent Service) | HR/Internal |
| [GitHub - Azure-Samples/agent-openai-java-banking-assistant: multi-agents banking assistant with Java and Semantic Kernel](Semantic Kernel) | FSI |
| [GitHub - Azure-Samples/moneta-agents](Semantic Kernel) | FSI |
 