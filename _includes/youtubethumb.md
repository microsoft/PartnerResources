{% comment %}

use include.type to switch between thumbnail and embedded iframe player

----------------------------------------------------
    generic youtube link for academies
    mqdefault: thumbnail is 320x180, no black bars 16:9
    0.jpg: is 480x360, typically has back bars
    maxresdefault: 1280x720, but not always there
----------------------------------------------------

{% endcomment %}

{% assign defaultType = "thumbnail" %}
{% if include.type %}
    {% assign defaultType = include.type %}
{% endif %}

{% if defaultType == "thumbnail" %}

<a alt="{{ page.title }}" href="https://www.youtube.com/watch?v={{ page.youtubeid }}" {% if include.target.size > 0 %}target={{target}}{% endif %}><img src="https://img.youtube.com/vi/{{ page.youtubeid }}/mqdefault.jpg" style="border: 1px solid black;"/><br/>Watch on YouTube</a>

{% else %}

<iframe width="720" height="405" src="http://www.youtube.com/embed/{{ page.youtubeid }}" frameborder="0" allowfullscreen></iframe>

{% endif %}