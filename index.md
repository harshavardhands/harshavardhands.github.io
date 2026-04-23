---
layout: default
title: Home
---
Notes on LLMs, system design, and architecture.
---

## 📝 Articles

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url | relative_url }})

<small>{{ post.date | date: "%B %d, %Y" }}</small>

{{ post.excerpt | strip_html | truncate: 200 }}

---

{% endfor %}
