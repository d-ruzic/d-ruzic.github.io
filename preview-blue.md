---
layout: default
theme: blue
preview: true
permalink: /preview-blue/
---
{% comment %}Trial page: same content as index.md, accent colour "blue". Delete when done.{% endcomment %}
{% capture home %}{% include_relative index.md %}{% endcapture %}
{{ home | split: "---" | last }}
