---
layout: default
title: Página Inicial
---

<style>
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f9f9f9;
  color: #333;
  margin: 0;
  padding: 0;
}

h1, h2 {
  color: #2c3e50;
}

.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 24px;
  padding: 40px;
  max-width: 1200px;
  margin: auto;
}

.card {
  background-color: #fff;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0,0,0,0.08);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0,0,0,0.12);
}

.card img {
  width: 100%;
  height: 180px;
  object-fit: cover;
}

.card-content {
  padding: 20px;
}

.card-title {
  font-size: 1.3em;
  font-weight: bold;
  margin-bottom: 10px;
  color: #34495e;
}

.card-date {
  font-size: 0.85em;
  color: #888;
  margin-bottom: 10px;
}

.card-content p {
  font-size: 0.95em;
  line-height: 1.5;
  color: #555;
}
</style>



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
