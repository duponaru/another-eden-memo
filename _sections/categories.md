---
title: Categories
subtitle: 
layout: "page"
icon: fa-book
order: 2
---

<!-- <ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul> -->

{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li><a>{{ post.title }}</a></li>    
      <!-- <li><a href="{{ post.url }}">{{ post.title }}</a></li> -->
    {% endfor %}
  </ul>
{% endfor %}