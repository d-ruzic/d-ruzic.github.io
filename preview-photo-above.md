---
layout: default
photo_position: above
preview: true
permalink: /preview-photo-above/
---
{% comment %}Trial page: same content as index.md, photo placed "above". Delete when done.{% endcomment %}
{% capture home %}{% include_relative index.md %}{% endcapture %}
{{ home | split: "---" | last }}
