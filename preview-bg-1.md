---
layout: default
preview: true
permalink: /preview-bg-1/
intro_bg:
  image: "/assets/img/intro-save-dunav.jpg"
  author: "Joergsam"
  source: "https://commons.wikimedia.org/wiki/File:Belgrad_PobednikStatue_Mit_Save_Und_Donau.jpg"
  license: "CC BY-SA 4.0"
  license_url: "https://creativecommons.org/licenses/by-sa/4.0/"
  position: "75% bottom"
---
{% comment %}Trial page: same content as index.md, with a Pobednik sketch behind the name. Delete when done.{% endcomment %}
{% capture home %}{% include_relative index.md %}{% endcapture %}
{{ home | split: "---" | last }}
