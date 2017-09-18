---
title: "Cuentos"
permalink: /cuentos/ 
layout: splash
author_profile: false
header: 
  overlay_image: /assets/images/pages/cuentos.jpg
---

# Cuentos 

{% assign sorted_posts = site.categories.Cuentos | sort:"title" %}
{% for post in sorted_posts %}
  {% include archive-single.html %}
{% endfor %}