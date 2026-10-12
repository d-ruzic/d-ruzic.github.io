---
layout: default
preview: true
permalink: /preview-bg-sava/
intro_bg:
  image: "/assets/img/intro-sava.jpg"
  author: "Aleksandr Petukhov"
  source: "https://commons.wikimedia.org/wiki/File:The_Victor_and_the_Sava_river.jpg"
  license: "CC BY-SA 4.0"
  license_url: "https://creativecommons.org/licenses/by-sa/4.0/"
---
{% comment %}Trial page: same content as index.md, with a Pobednik sketch behind the name. Delete when done.{% endcomment %}
{% capture home %}{% include_relative index.md %}{% endcapture %}
{{ home | split: "---" | last }}
