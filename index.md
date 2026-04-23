---
layout: default
title: Home
---
Notes on LLMs, system design, and architecture.
---

## 📝 Articles

{% for post in site.posts %}
<div style="margin-bottom: 2rem; padding: 1rem; border: 1px solid #eee; border-radius: 8px;">

### [{{ post.title }}]({{ post.url | relative_url }})

<small>{{ post.date | date: "%B %d, %Y" }}</small>

<p>{{ post.excerpt | strip_html | truncate: 180 }}</p>

<a href="{{ post.url | relative_url }}">Read more →</a>

</div>
{% endfor %}
