---
layout: default
title: Home
---

# Notes on LLMs, system design, and architecture.

## 📝 Articles

{% for post in site.posts %}
<article style="margin-bottom: 2rem; padding-bottom: 1.5rem; border-bottom: 1px solid #e5e7eb;">
  <h2 style="margin: 0 0 0.35rem 0; font-size: 1.5rem; font-weight: 700;">
    <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: #1d4ed8;">
      {{ post.title }}
    </a>
  </h2>

  <p style="margin: 0 0 0.75rem 0; color: #6b7280; font-size: 0.95rem;">
    {{ post.date | date: "%B %d, %Y" }}
  </p>

  <p style="margin: 0 0 0.9rem 0; line-height: 1.7; color: #374151;">
    {{ post.excerpt | strip_html | truncate: 180 }}
  </p>

  <a href="{{ post.url | relative_url }}" style="font-weight: 600; text-decoration: none; color: #1d4ed8;">
    Read more →
  </a>
</article>
{% endfor %}
