---
layout: page
title: Blog
permalink: /blog/
---

# Blog

{% if site.posts.size > 0 %}
{% for post in site.posts %}
- {{ post.date | date: "%d %B %Y" }} — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% else %}
Posts will appear here when published.
{% endif %}
