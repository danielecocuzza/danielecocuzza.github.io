---
layout: page
title: Blog
permalink: /blog/
---

{% for post in site.posts %}
- <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  <small> · {{ post.date | date: "%d %b %Y" }}</small>
{% endfor %}
