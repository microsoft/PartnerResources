---
layout: page
title: All Azure Plans
permalink: /azure/
tags:
- azure
---

<h2 id="tags-index">Azure Learning Plans</h2>

{% capture site_tags %}
{% for tag in site.tags %}
    {% if tag %}
        {{ tag | first }}
        {% unless forloop.last %}|{% endunless %}
    {% endif %}
{% endfor %}
{% endcapture %}
{% assign docs_tags = "" %}
{% for doc in site.docs %}
    {% assign ttags = doc.tags | join:'|' | append:'|' %}
    {% assign docs_tags = docs_tags | append:ttags %}
{% endfor %}
{% assign all_tags = site_tags | append:docs_tags %}
{% assign tags_list = all_tags | replace: "||", "|" | split:'|' | uniq | sort | compact %}
{% assign all_docs = site.docs | sort: "title" %}
{% assign filtered_docs = all_docs | where_exp: "doc","doc.tags contains 'learning plan'" %}

{% assign current_docs = "" | split: ',' %}
{% for doc in filtered_docs %}
{% unless doc.tags contains 'deprecated' %}
{% assign current_docs = current_docs | push: doc %}
{% endunless %}
{% endfor %}

<h3><a href="{{- site.baseurl -}}/azure/appdev/">AppDev</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'appdev' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.date | date_to_xmlschema -}}"> {{- doc.date | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}

<h3><a href="{{- site.baseurl -}}/azure/data-analytics-ai/">Data, Analytics, and AI</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'data, analytics, and ai' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.date | date_to_xmlschema -}}"> {{- doc.date | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}

<h3><a href="{{- site.baseurl -}}/azure/infrastructure/">Infrastructure</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'infrastructure' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.date | date_to_xmlschema -}}"> {{- doc.date | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}

<h3><a href="{{- site.baseurl -}}/azure/iot/">IoT</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'iot' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.date | date_to_xmlschema -}}"> {{- doc.date | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}

<h3><a href="{{- site.baseurl -}}/azure/azure-marketplace/">Azure Marketplace</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'marketplace' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.date | date_to_xmlschema -}}"> {{- doc.date | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}