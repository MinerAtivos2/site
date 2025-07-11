---
layout: default
title: Página Inicial
---

# Bem-vindo ao meu site com Jekyll no GitHub Pages!

Este site foi criado diretamente pelo navegador usando GitHub Pages e Jekyll.

{% for post in site.posts %}
## {{ post.title }}📅 {{ post.date | date: "%d/%m/%Y" }}

{{ post.excerpt }}

---
{% endfor %}




---
layout: default
title: Página Inicial
---

<style>
.card-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}
.card {
  width: 300px;
  border: 1px solid #ddd;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 2px 2px 8px rgba(0,0,0,0.1);
}
.card img {
  width: 100%;
  height: 180px;
  object-fit: cover;
}
.card-content {
  padding: 15px;
}
.card-title {
  font-size: 1.2em;
  margin: 0 0 10px;
}
.card-date {
  font-size: 0.9em;
  color: #666;
}
</style>

# Últimos Posts

<div class="card-grid">
{% for post in site.posts %}
  <div class="card">
    <a href="{{ post.url }}">
      <img src="{{ post.image | default: '/assets/img/default.jpg' }}" alt="Imagem do post">
    </a>
    <div class="card-content">
      <div class="card-title">{{ post.title }}</div>
      <div class="card-date">{{ post.date | date: "%d/%m/%Y" }}</div>
      <p>{{ post.excerpt }}</p>
    </div>
  </div>
{% endfor %}
</div>
