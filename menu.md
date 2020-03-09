---
title: Menu
subtitle: 
layout: "page"
icon: fa-book
order: 3
---

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>