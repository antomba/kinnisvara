---
layout: default
title: Kategooriad
description: Kinnisvarablogi kategooriad koos postituste arvuga ja teemade kaupa koondatud artiklitega.
permalink: /kategooriad/
---

<section class="section">
  <h1>Kategooriad</h1>
  <ul>
    {% for category in site.categories %}
      <li><a href="#{{ category[0] | slugify }}">{{ category[0] }}</a> ({{ category[1].size }})</li>
    {% endfor %}
  </ul>
</section>

{% for category in site.categories %}
  <section class="section" id="{{ category[0] | slugify }}">
    <h2>{{ category[0] }} ({{ category[1].size }})</h2>
    <ul class="post-list">
      {% for post in category[1] %}
        <li class="post-card">
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          <p class="post-meta">{{ post.date | date: "%d.%m.%Y" }} · {{ post.description }}</p>
        </li>
      {% endfor %}
    </ul>
  </section>
{% endfor %}
