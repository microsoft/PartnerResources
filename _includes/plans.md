{% comment %}
----------------------------------------------------
Get a list of all plans based on parameteres passed 
into this include file:

- include.includemethod         all/any - all=all tags must match
- include.includetags
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
{% assign includeTags = include.includetags | split:'|' | compact %}
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
{% if sortorder == "asc" %}
    {% assign all_docs = site.docs | sort: 'title' %}
{% else %}
    {% assign all_docs = site.docs | sort: 'title' | reverse %}
{% endif %}

{% assign filtered_docs = all_docs | where_exp: "doc","doc.tags contains 'learning plan'" %}
{% assign current_docs = "" | split: ',' %}


{% comment %}
----------------------------------------------------
filter plans based on tags
----------------------------------------------------
{% endcomment %}
{% if includeMethod == 'all' %}
    {% for doc in filtered_docs %}
        {% unless doc.tags contains "deprecated" %}
        {% assign uniquedoctags = doc.tags | uniq | sort %}
        {% assign concatplans = uniquedoctags | concat: includeTags | uniq %}
        {% comment %}
            To see if a document is a match, we'll concat includeTags and doc.tags --
            if they have the same number of tags, the document matches the filter so will be included
        {% endcomment %}
        {% if uniquedoctags.size == concatplans.size %}
        {% assign current_docs = current_docs | push: doc %}
        {% endif %}
        {% endunless %}
    {% endfor %}
{% else %}
    {% comment %}
        'any' include method will include a plan if any tag matches
    {% endcomment %}
    {% for doc in filtered_docs %}
        {% for includetag in includeTags %}
            {% unless doc.tags contains "deprecated" %}
            {% if doc.tags contains includetag %}
            {% assign current_docs = current_docs | push: doc %}
            {% endif %}
            {% endunless %}
        {% endfor %}
    {% endfor %}
{% endif %}
{% assign current_docs = current_docs | uniq %}

{% comment %}
----------------------------------------------------
    additional sorting
    todo: check sortfield for nulls - site will 
    not build if a page is missing specified sortfield
----------------------------------------------------
{% endcomment %}
{% if sortfield != "title" %}
    {% if sortorder == "asc" %}
        {% assign current_docs = current_docs | sort: sortfield %}
    {% else %}
        {% assign current_docs = current_docs | sort: sortfield | reverse %}
    {% endif %}
{% endif %}
{% comment %}
----------------------------------------------------
{% endcomment %}

{% for doc in current_docs %}
{% assign uniquedoctags = doc.tags | uniq | sort %}
<div class="tag-entry">
    <div><a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a></div>
    <div>{% for tag in uniquedoctags %}<span style="font-size:12px" class="badge badge-{{ site.tag_color }}"><a style="cursor:pointer; color:white" href="{% if site.tag_search_endpoint %}{{ site.tag_search_endpoint }}{{ tag }}{% else %}{{ site.url }}{{ site.baseurl }}/tags#{{ tag }} {% endif %}">{{ tag }}</a></span>{% endfor %}</div>
    <div>{{ doc.description }}</div>
    {% if doc.updated %}
    <div class="docupdated">Updated <time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time></div>
    {% endif %}
</div>
<div style="padding-bottom: 20px;"></div>
{% endfor %}

{% include toc.html %}
{% include permalinks.html %}
{% include tags.html %}
