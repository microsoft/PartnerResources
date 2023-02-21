{% comment %}
----------------------------------------------------
Get a list of all plans based on parameteres passed 
into this include file:

- include.includemethod         all/any - all=all tags must match
- include.includeSection
- include.sortfield
- include.sortorder

Any number of plan filters can be passed in via page.includeplans

'any' acts like an 'or' and will match any tag
'all' acts like an 'and' and doc must have all tags
----------------------------------------------------
{% endcomment %}

{% assign includeMethod = "all" %}
{% if include.includemethod %}
    {% assign includeMethod = include.includemethod %}
{% endif %}
{% assign includeSection = include.includeSection | split:'|' | compact %}
{% assign sortfield = "title" %}
{% if include.sortfield %}
    {% assign sortfield = include.sortfield %}
{% endif %}
{% assign sortorder = "asc" %}
{% if include.sortorder == "desc" %}
    {% assign sortorder = "desc" %}
{% endif %}

{% comment %}
----------------------------------------------------
Get all tags and base documents
----------------------------------------------------
{% endcomment %}
{% assign all_docs = site.docs | sort: "title" %}
{% assign filtered_docs = all_docs | where_exp: "doc","doc.tags contains 'learning plan'" %}
{% assign current_docs = "" | split: ',' %}
{% for doc in filtered_docs %}
{% unless doc.tags contains 'deprecated' %}
{% assign current_docs = current_docs | push: doc %}
{% endunless %}
{% endfor %}

{% comment %}
----------------------------------------------------
Loop through TOC
----------------------------------------------------
{% endcomment %}
{% for section in site.data.toc %}
{% capture sectionUrl %}{{ section.url | replace: "/", "" }}{% endcapture %}
{% capture pageUrl %}{{ page.url | replace: "/", "" }}{% endcapture %}

{% for entry in section.links %}

{% assign tocTitle = entry.title | upcase %}
{% assign sectionTitle = includeSection[0] | upcase %}
{% if tocTitle == sectionTitle %}

<div><h2><a href="{{- site.baseurl -}}/{{ entry.url }}">{{ page.title }}</a></h2></div>

{% for child in entry.children %}
<div><h3 style="margin-top:20px; margin-bottom: 10px;"><a class="td-sidebar-link td-sidebar-link__page " id="m-{{ section.title | slugify }}-{{ entry.title | slugify }}-{{ child.title | slugify }}" href="{% if child.url %}{{ site.baseurl }}/{{ child.url }}{% else %}{{ child.external_url }}{% endif %}">{{ child.title }}</a></h3></div> 
{% comment %}
sort items by using the sort order in TOC
{% endcomment %}
{% assign sortfield = "title" %}
{% if child.sortfield %}
{% assign sortfield = child.sortfield %}
{% endif %}
{% assign current_docs = current_docs | sort: sortfield %}

{% for doc in current_docs %}
{% if doc.tags contains child.tag %}
<div class="tag-entry" style="padding-left:25px;">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a>
    {% if doc.updated %}
    <span class="docupdated" style="padding-left: 5px;">Updated <time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time></span>
    {% endif %}
    </div>
</div>
{% endif %}
{% endfor %}
{% endfor %}

{% endif %}
{% endfor %}
{% endfor %}

