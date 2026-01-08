---
layout: page
title: Mis Artículos
paginate: true
---

## Artículos detectados ok 2:

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
