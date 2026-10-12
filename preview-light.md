---
layout: default
theme: light
preview: true
permalink: /preview-light/
---
{% comment %}Trial page: same content as index.md, colour theme "light". Delete when done.{% endcomment %}
{% capture home %}{% include_relative index.md %}{% endcapture %}
{{ home | split: "---" | last }}
