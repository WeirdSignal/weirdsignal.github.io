---
layout: default
title: Accueil du Blog
---

# Bienvenue sur le blog de WeirdSignal !

<select id="tag-select" onchange="filterPosts()">
  <option value="">Tous les articles</option>
  {% for tag in site.tags %}
    <option value="{{ tag[0] | slugify }}">{{ tag[0] }}</option>
  {% endfor %}
</select>

<div id="posts">
  <ul>
  {% for post in site.posts %}
    <li class="post-item" data-tags="{% for tag in post.tags %}{{ tag | slugify }} {% endfor %}">
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
</div>

<script>
function filterPosts() {
  const select = document.getElementById("tag-select");
  const selectedTag = select.value;
  const posts = document.getElementsByClassName("post-item");

  for (let post of posts) {
    const tags = post.getAttribute("data-tags").split(" ");
    if (selectedTag === "" || tags.includes(selectedTag)) {
      post.style.display = "block";
    } else {
      post.style.display = "none";
    }
  }
}
</script>
