---
layout: default
title: Blogi
description: "Eesti kinnisvarablogi artiklid: turuülevaated, ostu- ja müügisoovitused, üüriteemad ning laenuriskide analüüs."
permalink: /blog/
---

<section class="section">
  <h1>Blogi</h1>
  <p>Kõik postitused kinnisvaraturu, ostmise, üürimise, finantseerimise ja renoveerimise teemadel.</p>
</section>

<section class="section">
  <h2>Leht 1</h2>
  <ul class="post-list">
    {% for post in site.posts limit:3 %}
      <li class="post-card">
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p class="post-meta">{{ post.date | date: "%d.%m.%Y" }} · {{ post.description }}</p>
      </li>
    {% endfor %}
  </ul>
  <nav class="pagination" aria-label="Lehitsemine">
    <span>Varasemad puuduvad</span>
    <a href="{{ '/blog/leht-2/' | relative_url }}">Järgmine leht</a>
  </nav>
</section>
