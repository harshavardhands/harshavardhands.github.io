---
layout: default
title: Home
---

# Welcome 👋

Notes on LLMs, system design, and architecture.

---

## 📝 Articles

{% if site.posts.size > 0 %}
<ul>
  {% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a><br>
    <small>{{ post.date | date: "%B %d, %Y" }}</small>
  </li>
  {% endfor %}
</ul>
{% else %}
<p>No articles found.</p>
{% endif %}
