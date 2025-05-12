---
layout: home
title: "Mi Blog"
---

# ¡Publicaciones Recientes!

{% for post in site.posts %}
<div class="post-preview">
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <small>{{ post.date | date: "%d/%m/%Y" }}</small>
  
  {% if post.image %}  <!-- Si el post tiene imagen -->
  <img src="{{ post.image }}" alt="{{ post.title }}" style="max-width: 300px; margin: 10px 0;">
  {% endif %}
  
  <p>{{ post.excerpt | truncate: 150 }}</p>  <!-- Muestra un resumen -->
</div>
<hr>
{% endfor %}