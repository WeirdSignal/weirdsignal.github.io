---
layout: home
title: Mon Blog
description: Un blog personnel pour partager mes idées et projets
author: Votre Nom  # Optional, but Minima often uses this for display
---

# Bienvenue sur mon blog

Voici mes derniers articles :

{% for post in site.posts %}
* [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%B %-d, %Y" }} {% if post.tags.size > 0 %} (Tags: {{ post.tags | join: ", " }}) {% endif %}
{% endfor %}
