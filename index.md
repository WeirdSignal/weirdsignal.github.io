---
layout: home
title: Mon Blog
description: Un blog personnel pour partager mes idées et projets
---
# Bienvenue sur mon blog

Voici mes derniers articles :

{% for post in site.posts %}
* [{{ post.title }}]({{ post.url | relative_url }}) ({{ post.date | date_to_string }}) {% if post.tags.size > 0 %}Tags: {{ post.tags | join: ", " }}{% endif %}
{% endfor %}
