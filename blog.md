---
layout: page
title: 
permalink: /blog/
---
<h1 class="section-title">Blog</h1>

<ul class="post-list timeline">
  {% for post in site.posts %}
    <li>
      <div class="post-card">
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="post-meta">{{ post.date | date: "%d %b %Y" }}</span>
      </div>
    </li>
  {% endfor %}
</ul>
