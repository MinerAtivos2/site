---
layout: home
title: "MinerAtivos"
description: "Análises e insights do mercado de ações brasileiro, com foco em dados."
---

# Bem-vindo ao MinerAtivos

Acompanhe as postagens mais recentes sobre o mercado financeiro, ações da B3 e estratégias baseadas em dados.

<div class="alert alert-success mt-4" role="alert">
  <h1 class="alert-heading fst-italic mb-3">Postagem em destaque</h1>
  <p style="text-align:justify;">Veja aqui a análise mais popular do nosso blog com dados técnicos e gráficos detalhados.</p>
  <div class="d-flex justify-content-end">
    <a class="btn btn-outline-success line-green stretched-link mt-3" href="/posts/postagem-destaque.html">Saiba mais</a>
  </div>
</div>

## Últimas postagens

<ul class="post-list">
  {% for post in site.posts limit:5 %}
    <li class="post">
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p class="post-meta">
        {{ post.date | date: "%d/%m/%Y" }}
      </p>
      <p>{{ post.excerpt }}</p>
      <a class="btn btn-outline-primary" href="{{ post.url | relative_url }}">Leia mais</a>
    </li>
  {% endfor %}
</ul>

---

### Siga-nos:

- 📺 [YouTube](https://www.youtube.com/channel/UCc3QiTGPzbeOva5vGjXqW3g)
- 📸 [Instagram](https://www.instagram.com/minerativos/)
- 🐦 [Twitter (X)](https://x.com/MinerAtivos)
- 💼 [LinkedIn](https://www.linkedin.com/company/minerativos)
