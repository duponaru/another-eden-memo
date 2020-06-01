---
title: Tags
subtitle: 
layout: "page"
icon: fa-book
order: 3
---

{% for category in site.tags %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <!-- <li><a>{{ post.title }}</a></li> -->
      <p><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></p>
    {% endfor %}
  </ul>
{% endfor %}