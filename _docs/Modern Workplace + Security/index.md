---
layout: page
title: All Modern Workplace and Security Plans
permalink: /modern-workplace/
tags:
- modern workplace
---

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

<h3><a href="{{- site.baseurl -}}/modern-workplace/management/">Management</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'modern workplace management' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}

<h3><a href="{{- site.baseurl -}}/modern-workplace/microsoft-teams/">Microsoft Teams</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'microsoft teams' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}

<h3><a href="{{- site.baseurl -}}/modern-workplace/security/">Security</a></h3>
{% for doc in current_docs %}
{% if doc.tags contains 'security' %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> (Updated <time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time>)</div>
</div>
{% endif %}
{% endfor %}