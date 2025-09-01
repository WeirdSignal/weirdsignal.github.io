---
layout: default
title: Accueil du Blog
---

# Bienvenue sur mon blog !

Voici les derniers articles publiés :

{% for post in site.posts %}
  * [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%d %B %Y" }}
{% endfor %}

{% plantuml %}
@startuml
Alice -> Bob: Hello
@enduml
{% endplantuml %}
