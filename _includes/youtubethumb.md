{% comment %}
----------------------------------------------------
    generic youtube link for academies
    mqdefault: thumbnail is 320x180, no black bars
    0.jpg: is 480x360, typically has back bars
    maxresdefault: 1280x720, but not always there
----------------------------------------------------
{% endcomment %}

[![{{ page.title }}](https://img.youtube.com/vi/{{ page.youtubeid }}/mqdefault.jpg)](https://www.youtube.com/watch?v={{ page.youtubeid }})