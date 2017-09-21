---
title: "Colombia"
permalink: /colombia/ 
layout: "splash"
header:
  overlay_color: "#000"
  overlay_filter: "0"
  overlay_image: /assets/images/colombia.jpg
---


{% assign sorted_posts = site.categories.Colombia | sort:"title" %}
{% for post in sorted_posts %}
   {% include archive-single.html %}
{% endfor %}

