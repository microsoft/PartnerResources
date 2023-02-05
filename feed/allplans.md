---
layout: null
sitemap: false
permalink: /feed/allplans
---

{% assign all_docs = site.docs %}
{% assign filtered_docs = all_docs | where_exp: "doc","doc.tags contains 'learning plan'" %}
{% assign tmp_docs = filtered_docs | sort: "url" %}

  {% for doc in tmp_docs %}
  {% unless doc.tags contains "deprecated" %}
  {% if doc.nav_exclude != true %}

  {{ doc.title }}, {{ doc.updated }}, {% assign tmp_sa = doc.path | split: "/" %}{{ tmp_sa[1] | xml_escape }},{{ doc.permalink | absolute_url | xml_escape }}<br/>

  {% endif %}
  {% endunless %}
  {% endfor %}
