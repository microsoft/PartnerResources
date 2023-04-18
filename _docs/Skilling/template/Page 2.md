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

{% include_relative pagenav.md %}

Welcome to the Workshop Template! This page is an example of using the resources.md include file to include learning plans/readiness resources that match the provided criteria:

Example of using resources.md include file:

## OLTP/OLAP database resources:

### Using compact visual style 

{% include resources.md 
    includetags="data, analytics, and ai|sql server" 
    includesecondtags="data, analytics, and ai|database" 
    includethirdtags="data, analytics, and ai|mysql" 
    includefourthtags="data, analytics, and ai|postgres" 
    includemethod="all" 
    showtags="false" 
    showdate="true" 
    visualstyle="compact" 
    showdescription="true"
%}

## Synapse, Databricks, and other analytical platform resources:

### Using normal visual style 

{% include resources.md 
    includetags="data, analytics, and ai|synapse" 
    includesecondtags="data, analytics, and ai|databricks" 
    includethirdtags="data, analytics, and ai|big data" 
    includefourthtags="data, analytics, and ai|cosmos db" 
    includemethod="all" 
    showtags="false" 
    showdate="true" 
    visualstyle="normal" 
    showdescription="true"
%}

##  Power BI and dashboards resources:

### Using normal visual style 

{% include resources.md 
    includetags="power bi" 
    includesecondtags="dashboards" 
    includemethod="all" 
    showtags="false" 
    showdate="true" 
    visualstyle="normal" 
    showdescription="true"
%}