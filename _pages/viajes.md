---
title: "Viajes"
permalink: /viajes/ 
layout: splash
author_profile: false
header:
  overlay_image: /assets/images/header3.jpg
feature_paises:
  - image_path: /assets/images/pages/divisas.jpg
    alt: "un poco de plata"
    title: "Venezuela"
    excerpt: "La tierra..."
    url: /venezuela/
    btn_class: "btn--inverse"
  - image_path: /assets/images/pages/ccsplc.jpg
    alt: "aeropuerto maiquetia"
    title: "Colombia"
    excerpt: "Colombia..."
    url: /colombia/
    btn_class: "btn--inverse"

---

{% include feature_row id="feature_paises" %}

{::comment}

{% assign sorted_posts = site.categories.Viajes | sort:"title" %}
{% for post in sorted_posts %}
   {% include archive-single.html %}
{% endfor %}



- [Venezuela]({{ site.url }}{{ site.baseurl }}/venezuela/)
- [Cali, Colombia]({{ site.url }}{{ site.baseurl }}/Aprendiendo-hacer-Patacones-en-Cali/)

# 2016

- [San Gil, Colombia]({{ site.url }}{{ site.baseurl }}/El-Canon-del-Chicamocha/)




this could be used to automatically generate the menu, but i'll have to think about how to add sites which are not posts (such as /venezuela/)

{% for post in site.categories.Viaje %}
  <p>
    {% capture currentyear %}{{post.date | date: "%Y"}}{% endcapture %}
    {% if currentyear != thisyear %}
      <h1>{{currentyear}}</h1>
      {% capture thisyear %}{{post.date | date: "%Y"}}{% endcapture %}
    {% endif %}
  </p>
  <ul>
    <li>
      <p>
        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title | escape }}
        </a>
      </p>
    </li>
  </ul>
{% endfor %}

{:/comment}