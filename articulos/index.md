---
layout: page
title: Mis Publicaciones
paginate: true
---

## Lista de artículos 101:

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a> 
      - {{ post.date | date: "%d/%m/%Y" }}
    </li>
  {% endfor %}
</ul>

{% if paginator.total_pages > 1 %}
<div class="pagination" style="margin-top: 20px; font-weight: bold;">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | relative_url }}">« Anterior</a>
  {% else %}
    <span style="color: #ccc;">« Anterior</span>
  {% endif %}

  <span style="margin: 0 15px;">Página {{ paginator.page }} de {{ paginator.total_pages }}</span>

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | relative_url }}">Siguiente »</a>
  {% else %}
    <span style="color: #ccc;">Siguiente »</span>
  {% endif %}
</div>
{% endif %}
