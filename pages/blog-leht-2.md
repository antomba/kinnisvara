---
layout: default
title: Blogi - leht 2
description: "Kinnisvarablogi varasemad artiklid: üüritootlus, laenuriskid ja ostja kontrollnimekirjad."
permalink: /blog/leht-2/
---

<section class="section">
  <h1>Blogi</h1>
  <p>Postituste arhiiv.</p>
</section>

<section class="section">
  <h2>Leht 2</h2>
  <ul class="post-list">
    {% for post in site.posts offset:3 limit:3 %}
      <li class="post-card">
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p class="post-meta">{{ post.date | date: "%d.%m.%Y" }} · {{ post.description }}</p>
      </li>
    {% endfor %}
  </ul>
  <nav class="pagination" aria-label="Lehitsemine">
    <a href="{{ '/blog/' | relative_url }}">Eelmine leht</a>
    <span>Järgmised puuduvad</span>
  </nav>
</section>
