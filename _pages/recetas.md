---
title: "Recetas"
permalink: /recetas/ 
layout: "splash"
---

# Cócteles

{% assign sorted_posts = site.categories.Recetas | sort:"title" %}
{% for post in sorted_posts %}
{% if post.tags contains "Coctel" %}
  <ul>
    <li>
      <p>
        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title | escape }}</a>
      </p>
    </li>
  </ul>
  {% endif %}
{% endfor %}


# Comida


{% assign sorted_posts = site.categories.Recetas | sort:"title" %}
{% for post in sorted_posts %}
{% if post.tags contains "Comida" %}
  <ul>
    <li>
      <p>
        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title | escape }}</a>
      </p>
    </li>
  </ul>
  {% endif %}
{% endfor %}
