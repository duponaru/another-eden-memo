---
title: Tags
subtitle: 
layout: "page"
icon: fa-book
order: 3
---
<!-- {% for category in site.tags %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %} -->

<ul>
  {% assign sorted_tags = site.tags | sort %}
  {% for tag in sorted_tags %}
    {% assign t = tag | first %}
    {% assign posts = tag | last %}
    <li>
      <a href="/tags/# {{ t | downcase | replace:' ','-'}}">
        {{t | downcase | replace:' ','-' }}
        <span>({{ posts | size }})</span>
      </a>
    </li>
  {% endfor %}
</ul>