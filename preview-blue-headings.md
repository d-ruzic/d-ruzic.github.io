---
layout: default
theme: blue-headings
preview: true
permalink: /preview-blue-headings/
---
{% comment %}Trial page: same content as index.md, with the paper-list subheadings in blue. Delete when done.{% endcomment %}
{% capture home %}{% include_relative index.md %}{% endcapture %}
{{ home | split: "---" | last }}
