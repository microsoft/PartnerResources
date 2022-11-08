---
nav_exclude: true
layout: page
title: Name of Workshop or Series
description: Short Description of Workshop - Subpage Name
permalink: /skilling/academy-template/academy-template-page-2
updated: 2022-01-21
showbreadcrumb: false
tags: 
 - workshop
 - template
---

# Workshop Template

##  Content

* [Page 1](/skilling/academy-template/academy-template-page-1)
* [Page 2](/skilling/academy-template/academy-template-page-2)
* [Page 3](/skilling/academy-template/academy-template-page-3)

Welcome to the Workshop Template!

Use each page to add content for each relevant section of the workshop. This might be based on topic, day, or other logical grouping.

Use the series.md include to automatically include items in the /content folder. For example:

{% include series.md 
    includetags="academy template|academy content" 
    includemethod="all" 
    sortfield="updated" sortorder="desc" showdate="true" showtags="true"
    visualstyle="normal"
%}

Any embedded resources that needed to added to the repo directly, such as PPTX or images, should be housed in the root assets folder in a subfolder with a short name. For example, Modern Analytics Academy has content in /assets/maa/filename.pptx; this is necessary to support Github pages deployment. Ideally, video content should be embedded or linked to. See the Modern Analytics Academy for samples on how to do this.

__Important!__ Don't forget to update the 'front-matter' at the top of the document (the content between ---). Update the name and permalink -- remember each page needs a unqiue permalink. See how the template simply addes to the permalink with the sub page name.

## Table of Contents

If your workshop or series has an agenda or table of contents, add that here. 

## Main Content

The main content goes here.

## Other Information

If you have additional information for your workshop, add it here. Keep this first page high level as an overview.

The below is an example of a table with lab choices. Modify or delete as needed for your workshop.

| Lab Name | Time | Content | 
|---|---|---|
| Azure Synapse Analytics and AI | 8 hours | [Lab](https://github.com/microsoft/MCW-Azure-Synapse-Analytics-and-AI/blob/master/Hands-on%20lab/HOL%20step-by%20step%20-%20Azure%20Synapse%20Analytics%20and%20AI.md) |
| Analytics In a Day - Synapse | 4 hours | [Lab](https://github.com/solliancenet/azure-synapse-analytics-day) |
| Simplifying data flows with Azure Data Factory | 8 hours | [Lab](https://github.com/solliancenet/tech-immersion-data-ai/blob/master/data-exp5/README.md) |
| Modern Data Warehouse with Azure Synapse Analytics, <br />Azure Databricks, Azure Data Factory, and Power BI | 4 hours | [Lab](https://github.com/solliancenet/tech-immersion-data-ai/blob/master/data-exp6/README.md) |
