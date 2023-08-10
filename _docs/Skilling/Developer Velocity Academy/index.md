---
layout: page
title: Developer Velocity Academy - Home
description: Developer Velocity Academy - Home
permalink: /skilling/developer-velocity-academy
updated: 2023-08-10
showbreadcrumb: true
navheadersonly: true
tags:
- azure
- app dev
- developer velocity academy
---

# Developer Velocity Academy - Home

Welcome to the Developer Velocity Academy.

[description / overview information on academy, nav structure, etc.]

Can use includes for items like navigation:

{% include_relative pagenav.md %}

To show all content in academy:

{% include series.md 
    includetags=developer velocity academy|academy content" 
    includemethod="all" 
    sortfield="sorttitle" sortorder="desc" showdate="false" 
    showtags="true" visualstyle="normal" 
%}
