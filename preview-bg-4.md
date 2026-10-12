---
layout: default
preview: true
permalink: /preview-bg-4/
intro_bg:
  image: "/assets/img/intro-vainqueur.jpg"
  author: "TermlessPlayer4"
  source: "https://commons.wikimedia.org/wiki/File:Le_vainqueur.jpg"
  license: "CC BY-SA 4.0"
  license_url: "https://creativecommons.org/licenses/by-sa/4.0/"

---
{% comment %}Trial page: same content as index.md, with a Pobednik sketch behind the name. Delete when done.{% endcomment %}
{% capture home %}{% include_relative index.md %}{% endcapture %}
{{ home | split: "---" | last }}
