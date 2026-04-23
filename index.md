---
layout: default
title: Home
---
# Notes on LLMs, system design, and architecture.
---

## 📝 Articles

{% for post in site.posts %}

<div style="margin-bottom: 2.5rem; padding-bottom: 1.5rem; border-bottom: 1px solid #eaeaea;">

  <h2 style="margin-bottom: 0.3rem;">
    <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: #2a7ae2;">
      {{ post.title }}
    </a>
  </h2>

  <small style="color: #666;">
    {{ post.date | date: "%B %d, %Y" }}
  </small>

  <p style="margin-top: 0.7rem; line-height: 1.6;">
    {{ post.excerpt | strip_html | truncate: 180 }}
  </p>

  <a href="{{ post.url | relative_url }}" style="font-weight: 500;">
    Read more →
  </a>

</div>

{% endfor %}
