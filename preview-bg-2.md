---
layout: default
preview: true
permalink: /preview-bg-2/
intro_bg:
  image: "/assets/img/intro-drone.jpg"
  author: "Ivanbuki"
  source: "https://commons.wikimedia.org/wiki/File:DJI_0136-12.jpg"
  license: "CC BY-SA 4.0"
  license_url: "https://creativecommons.org/licenses/by-sa/4.0/"
---
{% comment %}Trial page: same content as index.md, with a Pobednik sketch behind the name. Delete when done.{% endcomment %}
{% capture home %}{% include_relative index.md %}{% endcapture %}
{{ home | split: "---" | last }}
