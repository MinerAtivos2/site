---
layout: default
title: "MinerAtivos"
description: "Análises e insights do mercado de ações brasileiro, com foco em dados."
---

<!-- Bootstrap Container -->
<div class="container py-4">
  <!-- Navbar -->
  <header class="sticky-top">
    <nav class="navbar navbar-expand-xl navbar-dark bg-dark">
      <div class="container-fluid">
        <a class="navbar-brand fs-4 fw-bold text-white" href="/">MinerAtivos</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <a class="nav-link text-white" href="/sobre">Sobre</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-white" href="/metodologia">Metodologia</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-white" href="https://x.com/MinerAtivos" target="_blank">Twitter</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-white" href="https://www.instagram.com/minerativos/" target="_blank">Instagram</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>

  <!-- Introducao -->
  <div class="mt-4 mb-5">
    <h1 class="fw-bold">Bem-vindo ao MinerAtivos</h1>
    <p class="lead">Análises baseadas em dados, focadas em ativos da B3, com visão quantitativa e insights acionáveis.</p>
  </div>

  <!-- Posts em destaque -->
  <div class="row">
    {% for post in site.posts limit:6 %}
    <div class="col-lg-4 col-md-6 mb-4">
      <div class="card h-100 shadow-sm border-0">
        {% if post.image %}
        <img src="{{ post.image }}" class="card-img-top" alt="{{ post.title }}">
        {% endif %}
        <div class="card-body d-flex flex-column">
          <h5 class="card-title fw-bold">{{ post.title }}</h5>
          <p class="card-text text-muted small">{{ post.date | date: "%d/%m/%Y" }}</p>
          <p class="card-text">{{ post.excerpt | strip_html | truncate: 130 }}</p>
          <a href="{{ post.url | relative_url }}" class="btn btn-outline-primary mt-auto stretched-link">{{ post.date | date: "%d/%m/%Y" }}</a>
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
</div>

<!-- Bootstrap JS -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
