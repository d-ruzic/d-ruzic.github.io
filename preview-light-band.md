---
layout: default
theme: light-band
preview: true
permalink: /preview-light-band/
---
{% comment %}Trial page: same content as index.md, colour theme "light-band". Delete when done.{% endcomment %}
{% capture home %}{% include_relative index.md %}{% endcapture %}
{{ home | split: "---" | last }}
