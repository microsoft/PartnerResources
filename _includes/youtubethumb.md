{% comment %}
----------------------------------------------------
    generic youtube link for academies
    mqdefault: thumbnail is 320x180, no black bars
    0.jpg: is 480x360, typically has back bars
    maxresdefault: 1280x720, but not always there
----------------------------------------------------
{% endcomment %}

<!--
<a alt="{{ page.title }}" href="https://www.youtube.com/watch?v={{ page.youtubeid }}" {% if include.target.size > 0 %}target={{target}}{% endif %}><img src="https://img.youtube.com/vi/{{ page.youtubeid }}/mqdefault.jpg" style="border: 1px solid black;"/><br/>Watch on YouTube</a>
-->

<iframe width="720" height="405" src="https://www.youtube.com/embed/{{ page.youtubeid }}bh" frameborder="0" allowfullscreen></iframe>