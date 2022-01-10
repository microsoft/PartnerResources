---
layout: page
title: Data, Analytics, and AI Learning Plans
permalink: /azure/data-analytics-ai/
tags: 
- azure
- data, analytics, and ai
---

<h2 id="tags-index">Data & AI Learning Plans</h2>

{% capture site_tags %}{% for tag in site.tags %}{% if tag %}{{ tag | first }}{% unless forloop.last %},{% endunless %}{% endif %}{% endfor %}{% endcapture %}{% assign docs_tags = "" %}{% for doc in site.docs %}{% assign ttags = doc.tags | join:',' | append:',' %}{% assign docs_tags = docs_tags | append:ttags %}{% endfor %}
{% assign all_tags = site_tags | append:docs_tags %}{% assign tags_list = all_tags | split:',' | uniq | sort %}
{% assign all_docs = site.docs | sort: "title" %}

{% for doc in all_docs %}
{% if doc.tags contains "learning plan" and doc.tags contains "data, analytics, and ai" %}
{% unless doc.tags contains "deprecated" }
<div class="tag-entry">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a></div>
    <div>{% for tag in doc.tags %}<span style="font-size:12px" class="badge badge-{{ site.tag_color }}"><a style="cursor:pointer; color:white" href="{% if site.tag_search_endpoint %}{{ site.tag_search_endpoint }}{{ tag }}{% else %}{{ site.url }}{{ site.baseurl }}/tags#{{ tag }} {% endif %}">{{ tag }}</a></span>{% endfor %}</div>
    <div>{{ doc.description }}</div>
    <div>Updated <time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time></div>
</div>
<div style="padding-bottom: 30px;"></div>
{% endunless %}
{% endif %}
{% endfor %}