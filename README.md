# Kinnisvara Blogi (Jekyll + GitHub Pages)

Eestikeelne kinnisvarablogi, mis töötab GitHub Pages keskkonnas. Sisuhaldus toimub Markdown-failidega (`_posts` + YAML front matter).

## Kohalik käivitamine

Eeldused:
- Ruby
- Bundler

Käivita:

```bash
bundle install
bundle exec jekyll serve
```

Ava brauseris: `http://127.0.0.1:4000`

## Uue postituse lisamine

1. Loo fail kausta `_posts/` kujul `YYYY-MM-DD-pealkiri.md`.
2. Lisa front matter:

```yaml
---
title: "Postituse pealkiri"
date: 2026-02-24
description: "Lühikirjeldus 140-160 tähemärki."
categories: [Ostmine]
tags: [Tallinn, korter]
image: /assets/images/pilt.jpg
---
```

3. Kirjuta sisu Markdownis pealkirjade ja loenditega.

## Piltide lisamine

- Salvesta pildid kausta `assets/images/`.
- Viita pildile postituse front matteris väljal `image`.
- Kasuta võimalusel optimeeritud formaati (WebP/JPEG) ja mõistlikku resolutsiooni.

## Deploy GitHub Pagesis

Projekt kasutab `github-pages` gem'i ning GitHub Pagesi toetatud Jekylli pluginaid (`jekyll-feed`, `jekyll-sitemap`).

Tüüpiline voog:
1. Push `main` harusse.
2. GitHub Pages buildib saidi automaatselt.
3. Sait avaldatakse Pages seadetes määratud allikast.

## Custom domain (CNAME)

1. Lisa reposti juurkausta fail `CNAME` (nt `www.sinudomeen.ee`).
2. Lisa domeeni DNS-is vajalikud kirjed (A/ALIAS/CNAME vastavalt GitHub juhistele).
3. Kontrolli GitHub Pages seadetes, et custom domain on aktiivne ja HTTPS sisse lülitatud.
