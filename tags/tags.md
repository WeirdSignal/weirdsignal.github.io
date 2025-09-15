---
layout: default
title: Tags
permalink: /tags/
---

# Tous les tags

<ul>
{% for tag in site.tags %}
  <li>
    <a href="#{{ tag[0] | slugify }}">{{ tag[0] }}</a> ({{ tag[1].size }})
  </li>
{% endfor %}
</ul>

{% for tag in site.tags %}
  <h2 id="{{ tag[0] | slugify }}">{{ tag[0] }}</h2>
  <ul>
    {% for post in tag[1] %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span>({{ post.date | date: "%B %d, %Y" }})</span>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
