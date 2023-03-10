{% comment %}
----------------------------------------------------
    generic youtube link for academies
    mqdefault: thumbnail is 320x180, no black bars
    0.jpg: is 480x360, typically has back bars
    maxresdefault: 1280x720, but not always there
----------------------------------------------------
{% endcomment %}

<a href="https://www.youtube.com/watch?v={{ doc.youtubeid }}" {% if include.target.size > 0 %}target={{target}}{% endif %}>Watch on YouTube:</br><img src="https://img.youtube.com/vi/{{ doc.youtubeid }}/mqdefault.jpg" style="border: 1px solid black;"/></a>