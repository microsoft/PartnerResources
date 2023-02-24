---
nav_exclude: true
layout: page
title: Microsoft Teams Academy
description: Microsoft Teams Academy
permalink: /skilling/microsoft-teams-academy
updated: 2023-02-27
showbreadcrumb: true
tags: 
 - microsoft teams academy
 - intro
---

# Microsoft Teams Academy

Welcome to the academy template. This index page is the 'home' page of the academy, and may contain any information about the entire academy, links to pages/subcontent, etc.

Please see the other workshops for examples of using headers, footers, and other callouts.

__Pages__ refer to all of the pages within the individual academy. In this case, the sample academy has 3 pages to help organize the academy into 3 logical sections. The pages are intended to help navigation within the academy. Include a tag with the academy name and 'page' to specify a page; for example, "sample academy page."

__Content__ are individual and discrete pieces of content within the academy. A good example would be a single YouTube video or an article/code sample. Typically, content will show on one or more pages, and if tagged appropriately, may even show on other academies. Include a tag with the academy name and 'content' to specify a piece of content; for example, "sample academy content." 

The tagging is important because the site is built by referencing the tags.

## All Content

{% include series.md 
    includetags="microsoft teams academy|academy content" 
    includemethod="all" 
    sortfield="sorttitle" sortorder="asc" showdate="true" showtags="true" 
    visualstyle="tiny"
%}

## Additional Content

Any embedded resources that needed to added to the repo directly, such as PPTX or images, should be housed in the root assets folder in a subfolder with a short name. For example, Modern Analytics Academy has content in /assets/maa/filename.pptx; this is necessary to support Github pages deployment. Ideally, video content should be embedded or linked to. See the Modern Analytics Academy for samples on how to do this.

__Important!__ Don't forget to update the 'front-matter' at the top of the document (the content between ---). Update the name and permalink -- remember each page needs a unqiue permalink. See how the template simply addes to the permalink with the sub page name.


