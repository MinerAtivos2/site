---
layout: default
title: Página Inicial
---

# Bem-vindo ao meu site com Jekyll no GitHub Pages!

Este site foi criado diretamente pelo navegador usando GitHub Pages e Jekyll.

{% for post in site.posts %}
## [{{ post.title }}📅 {{ post.date | date: "%d/%m/%Y" }}

{{ post.excerpt }}

---
{% endfor %}
