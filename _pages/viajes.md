---
title: "Viajes"
permalink: /viajes/ 
layout: "splash"
---

# 2017

- [Venezuela]({{ site.url }}{{ site.baseurl }}/venezuela/)
- [Cali, Colombia]({{ site.url }}{{ site.baseurl }}/Aprendiendo-hacer-Patacones-en-Cali/)


{::comment}
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