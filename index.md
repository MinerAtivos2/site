---
layout: default
title: Página Inicial
---

# 📰 Últimos Posts

<div class="card-grid">
{% for post in site.posts %}
  <div class="card">
    <a href="{{ post.url }}">
      <img src="{{ post.image | default: '/assets/img/default.jpg' }}" alt="Imagem do post">
    </a>
    <div class="card-content">
      <div class="card-title">{{ post.title }}</div>
      <div class="card-date">📅 {{ post.date | date: "%d/%m/%Y" }}</div>
      <p>{{ post.excerpt }}</p>
    </div>
  </div>
{% endfor %}
</div>
