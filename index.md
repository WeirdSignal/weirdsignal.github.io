---
layout: default
title: Accueil du Blog
---

# Bienvenue sur le blog de WeirdSignal !

Les derniers articles :

{% for post in site.posts %}
  * [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%d %B %Y" }}
{% endfor %}
