---
layout: page
title: Best Practices for Structured Extraction from Documents Using Azure OpenAI
sorttitle: 8
description: >- 
    In a recent project, a customer needed to extract structured data from legal documents to populate a standardized form. The legal documents varied in length and structure, and the customer required consistent and accurate outputs that mapped directly to the expected form schema. The implemented solution leveraged Azure OpenAI to iteratively process document chunks and update the form output dynamically. A key component to successfully extract the correct output was using Structured Outputs to enforce the desired output fields to populate the form.
    This article outlines best practices derived from this project, with a focus on scalable methods, reliable structure enforcement, and iterative processing of unstructured legal data. These lessons learned can be leveraged for additional scenarios and document types beyond legal documents in various industries including:
    - Healthcare: patient record management, clinical data extraction
    - Finance: automated processing of financial statements, regulatory reporting
    - Insurance: claims processing, policy management
    - Supply chain logistics: extracting shipment details and tracking information from shipping documents

permalink: /skilling/ai-ml-academy/bestpractices/structured_output_extraction
updated: 2025-05-16
showbreadcrumb: true
tags:
- ai & ml academy
- academy content
- best practices
---
# {{ page.title }}

{{ page.description }}

[View Best Practices on GitHub](https://github.com/microsoft-partner-solutions-ai/best-practices/blob/main/structured_output_extraction.md)
