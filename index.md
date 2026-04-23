---
layout: default
title: Home
---

# Notes on LLMs, system design, and architecture.

## 📝 Articles

{% for post in site.posts %}
<article style="margin-bottom: 2rem; border-bottom: 1px solid #eee; padding-bottom: 1.5rem;">

  <h2>
    <a href="{{ post.url | relative_url }}">
      {{ post.title }}
    </a>
  </h2>

  <small>{{ post.date | date: "%B %d, %Y" }}</small>

  <p>
    {{ post.excerpt }}
  </p>

  <a href="{{ post.url | relative_url }}">Read more →</a>

</article>
{% endfor %}
