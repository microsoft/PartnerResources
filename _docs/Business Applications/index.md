---
layout: page
title: All Business Applications & Power Platform Plans
permalink: /business-applications/
tags:
- buiness applications
---

<h2 id="tags-index">Business Applications & Power Platform</h2>

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

<h3><a href="{{- site.baseurl -}}/business-applications/customer-data-platform/">Customer Data Platform</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'customer data platform' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}

<h3><a href="{{- site.baseurl -}}/business-applications/customer-engagement/">Customer Engagement</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'customer engagement' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}

<h3><a href="{{- site.baseurl -}}/business-applications/finance-and-operations/">Finance & Operations</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'finance and operations' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}

<h3><a href="{{- site.baseurl -}}/business-applications/isv-connect/">ISV Connect</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'isv connect' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}

<h3><a href="{{- site.baseurl -}}/business-applications/mixed-reality/">Mixed Reality</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'mixed reality' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}

<h3><a href="{{- site.baseurl -}}/business-applications/power-platform/">Power Platform</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'power platform' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}

<h3><a href="{{- site.baseurl -}}/business-applications/small-medium-business-smb/">Small Medium Business (SMB)</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'smb' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}