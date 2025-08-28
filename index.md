---
layout: home
title: Mon Blog
description: Un blog personnel pour partager mes idées et projets
---
# Bienvenue sur mon blog

Voici mes derniers articles :

{% for post in site.posts limit:5 %}
- [{{ post.title }}]({{ post.url | relative_url }})  
  *Publié le {{ post.date | date: "%d %B %Y" }}*  
  {{ post.excerpt | strip_html | truncate: 100 }}
{% endfor %}
