---
layout: page
title: Mis Publicaciones Paginadas
---

## Artículos:

<ul>
  {% for post in paginator.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a> 
      - {{ post.date | date: "%d/%m/%Y" }}
    </li>
  {% endfor %}
</ul>

{% if paginator.total_pages > 1 %}
<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | relative_url }}">« Anterior</a>
  {% else %}
    <span>« Anterior</span>
  {% endif %}

  <span> Página {{ paginator.page }} de {{ paginator.total_pages }} </span>

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | relative_url }}">Siguiente »</a>
  {% else %}
    <span>Siguiente »</span>
  {% endif %}
</div>
{% endif %}
