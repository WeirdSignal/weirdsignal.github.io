---
layout: default
title: Tags
permalink: /tags/
---

# Tous les tags

<select id="tag-select" onchange="filterPosts()">
  <option value="">Tous les articles</option>
  {% for tag in site.tags %}
    <option value="{{ tag[0] | slugify }}">{{ tag[0] }}</option>
  {% endfor %}
</select>

<div id="posts">
  {% for tag in site.tags %}
    <div class="tag-section" id="{{ tag[0] | slugify }}">
      ## {{ tag[0] }} ({{ tag[1].size }})
      <ul>
        {% for post in tag[1] %}
          <li>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            <span>({{ post.date | date: "%B %d, %Y" }})</span>
          </li>
        {% endfor %}
      </ul>
    </div>
  {% endfor %}
</div>

<script>
function filterPosts() {
  const select = document.getElementById("tag-select");
  const selectedTag = select.value;
  const sections = document.getElementsByClassName("tag-section");

  for (let section of sections) {
    if (selectedTag === "" || section.id === selectedTag) {
      section.style.display = "block";
    } else {
      section.style.display = "none";
    }
  }
}
</script>
