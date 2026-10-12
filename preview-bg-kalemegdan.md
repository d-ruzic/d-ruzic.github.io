---
layout: default
preview: true
permalink: /preview-bg-kalemegdan/
intro_bg:
  image: "/assets/img/intro-kalemegdan.jpg"
  author: "Janos Guljas"
  source: "https://commons.wikimedia.org/wiki/File:Pobednik_monument,_Kalemegdan,_Belgrade.jpg"
  license: "CC BY-SA 3.0"
  license_url: "https://creativecommons.org/licenses/by-sa/3.0/"
---
{% comment %}Trial page: same content as index.md, with a Pobednik sketch behind the name. Delete when done.{% endcomment %}
{% capture home %}{% include_relative index.md %}{% endcapture %}
{{ home | split: "---" | last }}
