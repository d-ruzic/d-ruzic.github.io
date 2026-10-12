---
layout: default
preview: true
permalink: /preview-bg-3/
intro_bg:
  image: "/assets/img/intro-guardian.jpg"
  author: "Petko Zaric"
  source: "https://commons.wikimedia.org/wiki/File:Guardian_of_the_city.jpg"
  license: "CC BY-SA 4.0"
  license_url: "https://creativecommons.org/licenses/by-sa/4.0/"
  position: "70% bottom"
---
{% comment %}Trial page: same content as index.md, with a Pobednik sketch behind the name. Delete when done.{% endcomment %}
{% capture home %}{% include_relative index.md %}{% endcapture %}
{{ home | split: "---" | last }}
