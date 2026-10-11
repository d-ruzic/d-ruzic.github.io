---
layout: default
photo_position: name
preview: true
permalink: /preview-photo-name/
---
{% comment %}Trial page: same content as index.md, photo placed "name". Delete when done.{% endcomment %}
{% capture home %}{% include_relative index.md %}{% endcapture %}
{{ home | split: "---" | last }}
