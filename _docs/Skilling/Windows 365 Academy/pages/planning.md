---
nav_exclude: true
layout: page
title: Windows 365 Academy - Planning
sorttitle: Windows 365 Academy - Planning
description: Windows 365 Academy - Planning
permalink: /skilling/windows-365-academy/planning
updated: 2022-03-01
showbreadcrumb: false
tags: 
 - academy page
 - windows 365 academy
 - planning
---

# Windows 365 Academy - Planning

Welcome to the workshop template. Please see the other workshops for examples of using headers, footers, and other callouts.

Changes to the left nav can be made in the /_data/toc.yml file.

##  Content

Welcome to the Workshop Template!

Use each page to add content for each relevant section of the workshop. This might be based on topic, day, or other logical grouping.

Use the series.md include to automatically include items in the /content folder. For example:

{% include series.md 
    includetags="windows 365 academy|academy content|planning" 
    includemethod="all" 
    sortfield="updated" sortorder="desc" showdate="true" showtags="true" 
    visualstyle="normal"
%}

Any embedded resources that needed to added to the repo directly, such as PPTX or images, should be housed in the root assets folder in a subfolder with a short name. For example, Modern Analytics Academy has content in /assets/maa/filename.pptx; this is necessary to support Github pages deployment. Ideally, video content should be embedded or linked to. See the Modern Analytics Academy for samples on how to do this.

__Important!__ Don't forget to update the 'front-matter' at the top of the document (the content between ---). Update the name and permalink -- remember each page needs a unqiue permalink. See how the template simply addes to the permalink with the sub page name.

