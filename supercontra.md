---
layout: page
title: Mis Artículos
paginate: true
---

## Artículos detectados:

<ul>
  {% for post in paginator.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

{% if paginator.total_pages > 1 %}
  <div class="pagination">
    {% if paginator.previous_page %}
      <a href="{{ paginator.previous_page_path | relative_url }}">« Anterior</a>
    {% endif %}
    <span>Página {{ paginator.page }} de {{ paginator.total_pages }}</span>
    {% if paginator.next_page %}
      <a href="{{ paginator.next_page_path | relative_url }}">Siguiente »</a>
    {% endif %}
  </div>
{% endif %}
