---
title: "Cuentos"
permalink: /cuentos/ 
layout: splash
author_profile: false
header: 
  overlay_image: /assets/images/pages/cuentos.jpg
---

{% assign sorted_posts = site.categories.Cuentos | sort:"date" | reverse %}
{% for post in sorted_posts %}
  {% include archive-single.html %}
{% endfor %}