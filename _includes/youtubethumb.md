{% comment %}

use include.type to switch between thumbnail and embedded iframe player
    - iframe = iframe embedded player
    - thumbnail = original thumbnail link

---------------------------------------------------------------------
    mqdefault: thumbnail is 320x180, no black bars 16:9
    0.jpg: is 480x360, typically has back bars
    maxresdefault: 1280x720, but not always there depending on video
----------------------------------------------------------------------

{% endcomment %}

{% assign defaultType = "iframe" %}
{% assign thumbnailImage = "mqdefault.jpg" %}

{% if include.type %}
    {% assign defaultType = include.type %}
{% endif %}
{% if include.thumbnailImage %}
    {% assign thumbnailImage = include.thumbnailImage %}
{% endif %}

{% if defaultType == "thumbnail" %}

<a alt="{{ page.title }}" href="https://www.youtube.com/watch?v={{ page.youtubeid }}" {% if include.target.size > 0 %}target={{target}}{% endif %}><img src="https://img.youtube.com/vi/{{ page.youtubeid }}/{{ thumbnailimage }}" style="border: 1px solid black;"/><br/>Watch on YouTube</a>

{% else %}

<iframe width="720" height="405" src="http://www.youtube.com/embed/{{ page.youtubeid }}" frameborder="0" allowfullscreen></iframe>

{% endif %}