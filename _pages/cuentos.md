---
title: "Cuentos"
permalink: /cuentos/ 
layout: "splash"
---

# Cuentos 

{% assign sorted_posts = site.categories.Cuentos | sort:"title" %}
{% for post in sorted_posts %}
<ul>
  <li>
    <p>
      <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title | escape }}</a>
    </p>
  </li>
</ul>
{% endfor %}