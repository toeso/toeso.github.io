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
{% if post.tags contains "Coctel" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

{% assign sorted_posts = site.categories.Recetas | sort:"date" | reverse %}
{% for post in sorted_posts %}
{% if post.tags contains "Comida" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

{% assign sorted_posts = site.categories.Recetas | sort:"date" | reverse %}
{% for post in sorted_posts %}
{% if post.tags contains "Postre" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
