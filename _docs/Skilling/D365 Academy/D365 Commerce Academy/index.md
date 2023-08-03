---
layout: page
title: D365 Commerce Academy - Academy Home
sorttitle: 01
description: D365 Commerce Academy - Academy Home
permalink: /skilling/d365-academy/d365-commerce-academy/
updated: 2023-03-27
showbreadcrumb: true
tags:
- d365 academy
- d365
- dynamics
- d365 commerce academy
- academy page
- main page
---

# {{ page.title }}

Presentations:

* [Commerce In a Day - Updated 2023]({{ site.baseurl }}/assets/commerceacademy/Commerce%20In%20A%20Day%20Updated%202023.pdf)
* [E-Commerce Workshop Assets]({{ site.baseurl }}/assets/commerceacademy/E-Commerce%20Workshop%20Assets.zip)

Welcome to the D365 Commerce Academy. This page is currently under development.

All pages in this academy:

{% include series.md 
    includetags="d365 commerce academy|academy page" 
    includemethod="all" 
    sortfield="sorttitle" sortorder="asc" showdate="false" showtags="false" 
    visualstyle="navlist" showdescrip="false" removetext="D365 Commerce Academy - " 
%}

All sessions currently in this academy:

{% include series.md 
    includetags="d365 commerce academy|academy content" 
    includemethod="all" 
    sortfield="updated" sortorder="asc" showdate="false" 
    showtags="true" visualstyle="tiny" 
%}