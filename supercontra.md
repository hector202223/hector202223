---
layout: page
title: Mis Artículos
paginate: true
---

## Artículos detectados ok:

<ul>
  {% for post in paginator.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
