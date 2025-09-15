---
layout: default
title: Accueil du Blog
---

# Bienvenue sur le blog de WeirdSignal !

Les derniers articles :

<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%d %B %Y" }}
    {% if post.tags.size > 0 %}
      <br>Tags: 
      {% for tag in post.tags %}
        <a href="/tags/#{{ tag | slugify }}">{{ tag }}</a>{% unless forloop.last %}, {% endunless %}
      {% endfor %}
    {% endif %}
  </li>
{% endfor %}
</ul>
