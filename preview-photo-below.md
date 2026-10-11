---
layout: default
photo_position: below
preview: true
permalink: /preview-photo-below/
---
{% comment %}Trial page: same content as index.md, photo placed "below". Delete when done.{% endcomment %}
{% capture home %}{% include_relative index.md %}{% endcapture %}
{{ home | split: "---" | last }}
