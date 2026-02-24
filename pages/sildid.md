---
layout: default
title: Sildid
description: Kinnisvarablogi sildid koos postituste arvuga ja märksõnade järgi leitavate artiklitega.
permalink: /sildid/
---

<section class="section">
  <h1>Sildid</h1>
  <ul>
    {% for tag in site.tags %}
      <li><a href="#{{ tag[0] | slugify }}">#{{ tag[0] }}</a> ({{ tag[1].size }})</li>
    {% endfor %}
  </ul>
</section>

{% for tag in site.tags %}
  <section class="section" id="{{ tag[0] | slugify }}">
    <h2>#{{ tag[0] }} ({{ tag[1].size }})</h2>
    <ul class="post-list">
      {% for post in tag[1] %}
        <li class="post-card">
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          <p class="post-meta">{{ post.date | date: "%d.%m.%Y" }} · {{ post.description }}</p>
        </li>
      {% endfor %}
    </ul>
  </section>
{% endfor %}
