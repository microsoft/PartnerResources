{% comment %}
    There are 3 main variables in consideration. 
    1. Which assets to include? 
    2. Include all or any assets that match?
          'any' acts like an 'or' and will match any tag
          'all' acts like an 'and' and doc must have all tags
    3. Which tags to not show on list? (for cleanliness)

    These variables can be specified in 1 of 2 ways:
    1. Front matter at top of page
        - page.includeplans
        - page.includemethod
        - page.removetags
    2. OR, by passing parameters into this file directly, using:
        - include.includetags
        - include.includemethod
        - include.removetags
        - include.sortfield
        - include.sortorder
        - include.showdate
        - include.showtags
        - include.visualstyle
     
        For parameters, values are strings (no hyphens) 
        and delimited with | if needed. Example:
        includeplans="modern analytics academy | vignettes"
    
    If both are present, parameters passed in take precedence.

    visualstyle: controls the format for rendering the series.
    options include 
        - "normal" (default)
        - "compact" (titles/tags/dates/description)
        - "supercompact" (for long lists)

{% endcomment %}

{% assign assetsToInclude = "" | split: ',' %}
{% assign tagsToRemove = "" | split: ',' %}
{% assign includeMethod = "all" %}
{% assign sortField = "updated" %}
{% assign sortOrder = "desc" %}
{% assign showDate = "true" %}
{% assign showTags = "true" %}
{% assign visualStyle = "normal" %}

{% comment %}
----------------------------------------------------
    determine and set parameters based on source
----------------------------------------------------
{% endcomment %}

{% if include.includetags %}

    {% assign assetsToInclude = include.includetags | split:'|' | compact %}
    {% assign tagsToRemove = include.removetags | split:'|' | compact %}
    {% assign includeMethod = include.includemethod %}
    {% if include.sortfield %}
        {% assign sortField = include.sortfield %}
    {% endif %}
    {% if include.sortorder == "asc" %}
        {% assign sortOrder = "asc" %}
    {% endif %}
    {% if include.showdate == "false" %}
        {% assign showDate = "false" %}
    {% endif %}
    {% if include.visualstyle == "compact" %}
       {% assign visualStyle = "compact" %}
    {% endif %}
    {% if include.visualstyle == "supercompact" %}
       {% assign visualStyle = "supercompact" %}
    {% endif %}
    {% if include.showtags == "false" %}
       {% assign showTags = "false" %}
    {% endif %}

{% else %}

    {% assign assetsToInclude = page.includeplans %}
    {% assign tagsToRemove = page.removetags  %}
    {% assign includeMethod = page.includemethod %}
    {% if page.sortfield %}
        {% assign sortField = page.sortfield %}
    {% endif %}
    {% if page.sortorder == "asc" %}
        {% assign sortOrder = "asc" %}
    {% endif %}
    {% if page.showdate == "false" %}
        {% assign showDate = "false" %}
    {% endif %}
    {% if page.visualstyle == "compact" %}
       {% assign visualStyle = "compact" %}
    {% endif %}
    {% if page.visualstyle == "supercompact" %}
       {% assign visualStyle = "supercompact" %}
    {% endif %}
    {% if page.showtags == "false" %}
       {% assign showTags = "false" %}
    {% endif %}

{% endif %}

{% comment %}
----------------------------------------------------
    basic page variables/params and sorting
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

{% if sortOrder == "asc" %}
    {% assign all_docs = site.docs | sort: sortField %}
{% else %}
    {% assign all_docs = site.docs | sort: sortField | reverse %}
{% endif %}

{% assign filtered_docs = all_docs %}
{% assign current_docs = "" | split: ',' %}

{% comment %}
----------------------------------------------------
    additional filtering and sorting
----------------------------------------------------
{% endcomment %}

{% if includeMethod == 'all' %}
    {% for doc in filtered_docs %}
    {% unless doc.tags contains "deprecated" %}
    {% assign uniquedoctags = doc.tags | uniq | sort %}

    {% assign concatplans = uniquedoctags | concat: assetsToInclude | uniq %}
    {% comment %}
        To see if a document is a match, we'll concat assetsToInclude and doc.tags --
        if they have the same number of tags, the document matches the filter so will be included
    {% endcomment %}
    {% if uniquedoctags.size == concatplans.size %}
    {% assign current_docs = current_docs | push: doc %}
    {% endif %}
    {% endunless %}
    {% endfor %}
{% else %}
    {% for doc in filtered_docs %}
    {% for includetag in assetsToInclude %}
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

{% comment %}
    Filter tags for each doc, as specified in front matter
{% endcomment %}
{% assign filteredtags = "" | split: ',' %}
{% for tag in uniquedoctags %}
    {% assign foundFilteredTag = false %}
    {% for removetag in tagsToRemove %}
        {% if tag == removetag %}
           {% assign foundFilteredTag = true %}
        {% endif %}
    {% endfor %}
    {% if foundFilteredTag == false %}
        {% assign filteredtags = filteredtags | push: tag %}
    {% endif %}
{% endfor %}
{% assign filteredtags = filteredtags | uniq | sort %}

{% comment %}
----------------------------------------------------
    display results
----------------------------------------------------
{% endcomment %}

{% if visualStyle == "normal" %}
<div class="tag-entry" style="scroll-margin-top: 5rem;" id="{{ doc.title }}">
    <div>
        <a class="nav-entry" href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> 
        {% if doc.updated and showDate == true %}
            <span class="docupdated"><time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time></span>
        {% endif %}
    </div>
    {% if showTags == "true" %}
    <div style="padding-bottom: 5px;">{% for tag in filteredtags %}<span style="font-size:12px" class="badge badge-{{ site.tag_color }}"><a style="cursor:pointer; color:white" href="{% if site.tag_search_endpoint %}{{ site.tag_search_endpoint }}{{ tag }}{% else %}{{ site.url }}{{ site.baseurl }}/tags#{{ tag }} {% endif %}">{{ tag }}</a></span>{% endfor %}</div>
    {% endif %}
    <div>
    {% if doc.youtubeid %}<a href="https://www.youtube.com/watch?v={{ doc.youtubeid }}"><img width="160" src="https://img.youtube.com/vi/{{ doc.youtubeid }}/0.jpg" style="float:left; padding-right:15px;"/></a>
    {% endif %}
    {{ doc.description }} 
    <a href="{{- site.baseurl -}}{{- doc.url -}}">more &#187;</a> 
    </div>
</div>

<div style="clear:both; padding-top: 20px; padding-bottom: 0px;">
<hr/>
</div>
{% elsif visualStyle == "compact" %}
<div class="tag-entry" style="scroll-margin-top: 5rem;" id="{{ doc.title }}">
    <div>
        <a class="nav-entry" href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> 
        {% if doc.updated and showDate == "true" %}
            <span class="docupdated"><time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time></span>
        {% endif %}
    </div>
    {% if showTags == "true" %}
    <div style="padding-bottom: 5px;">{% for tag in filteredtags %}<span style="font-size:12px" class="badge badge-{{ site.tag_color }}"><a style="cursor:pointer; color:white" href="{% if site.tag_search_endpoint %}{{ site.tag_search_endpoint }}{{ tag }}{% else %}{{ site.url }}{{ site.baseurl }}/tags#{{ tag }} {% endif %}">{{ tag }}</a></span>{% endfor %}</div>
    {% endif %}
    <div>
    {{ doc.description }} 
    </div>
</div>

<div style="clear:both; padding-top: 15px; padding-bottom: 0px;">
</div>

{% elsif visualStyle == "supercompact" %}
<div class="tag-entry" style="scroll-margin-top: 5rem;" id="{{ doc.title }}">
    <div>
        <a class="nav-entry" href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> 
        {% if doc.updated and showDate == "true" %}
            <span class="docupdated"><time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time></span>
        {% endif %}
    </div>
</div>
<div style="clear:both; padding-top: 5px; padding-bottom: 0px;">
</div>
{% endif %}
{% endfor %}