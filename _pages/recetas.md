---
title: "Recetas"
permalink: /recetas/ 
layout: splash
author_profile: false
header: 
  overlay_image: /assets/images/pages/recetas.jpg
---

{% assign sorted_posts = site.categories.Recetas | sort:"date" | reverse %}
{% for post in sorted_posts %}
    {% include archive-single.html %}
{% endfor %}