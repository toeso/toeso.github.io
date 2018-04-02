---
title: "Viajes"
permalink: /viajes/ 
layout: splash
author_profile: false
header:
  overlay_image: /assets/images/pages/viajes.jpg
---

{% assign sorted_posts = site.categories.Viajes | sort:"date" | reverse %}
{% for post in sorted_posts %}
  {% include archive-single.html %}
{% endfor %}


{::comment}


feature_paises:
  - image_path: /assets/images/pages/venezuela.jpg
    alt: "bandera venezolana"
    title: "Venezuela"
    url: /venezuela/
  - image_path: /assets/images/pages/colombia.jpg
    alt: "bandera colombiana"
    title: "Colombia"
    url: /colombia/

{% include feature_row id="feature_paises" %}


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