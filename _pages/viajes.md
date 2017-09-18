---
title: "Viajes"
permalink: /viajes/ 
layout: "splash"
header:
  overlay_image: /assets/images/header3.jpg
  cta_label: "Venezuela"
  cta_url: "/venezuela/"
---

{% assign sorted_posts = site.categories.Viajes | sort:"title" %}
{% for post in sorted_posts %}
<ul>
  <li>
    <p>
      <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title | escape }}</a>
    </p>
  </li>
</ul>
{% endfor %}

{::comment}

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