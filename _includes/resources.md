{% comment %}
    
    Parameters:
        - include.includemethod         all/any - all=all tags must match
        - include.includetags
  
    Not yet implemented:
        - include.removetags            specifies tags to hide from display on list
        - include.sortfield
        - include.sortorder
        - include.showdate
        - include.showtags
        - include.showlink              show/hide deep link to content, default "true"
        - include.target                specify a target like target="_blank"
        - include.visualstyle           normal / compact / tiny
        - include.limit                 limit of number to display (no pagination support)
        - include.includesecondtags
        - include.includethirdtags
        - include.includefourthtags

    For parameters, values are strings (no hyphens) 
    and delimited with | if needed. Example:
    includetags="modern analytics academy | vignettes"

{% endcomment %}

{% assign tagsToInclude = "" | split: ',' %}
{% assign tagsToInclude = include.includetags | split:'|' | compact %}

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
{% comment %}
    Any number of plan filters can be passed in via include.includetags

    'any' acts like an 'or' and will match any tag
    'all' acts like an 'and' and doc must have all tags
{% endcomment %}

{% if include.includemethod == 'all' %}
    {% for doc in filtered_docs %}
    {% unless doc.tags contains "deprecated" %}
    {% assign uniquedoctags = doc.tags | uniq | sort %}
    {% assign concatplans = uniquedoctags | concat: tagsToInclude | uniq %}
    {% comment %}
        To see if a document is a match, we'll concat tagsToInclude and doc.tags --
        if they have the same number of tags, the document matches the filter so will be included
    {% endcomment %}
    {% if uniquedoctags.size == concatplans.size %}
    {% assign current_docs = current_docs | push: doc %}
    {% endif %}
    {% endunless %}
    {% endfor %}
{% else %}
    {% for doc in filtered_docs %}
    {% for includetag in tagsToInclude %}
    {% unless doc.tags contains "deprecated" %}
    {% if doc.tags contains includetag %}
    {% assign current_docs = current_docs | push: doc %}
    {% endif %}
    {% endunless %}
    {% endfor %}
    {% endfor %}
{% endif %}

{% assign current_docs = current_docs | uniq %}

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