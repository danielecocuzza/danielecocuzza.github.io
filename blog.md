---
layout: default
title: "AI Blog | Machine Learning, Computer Vision & Research"
description: "Articles and notes on Machine Learning, Computer Vision, Deep Learning, research and professional experience."
permalink: /blog/
---
<h1 class="hero-title">AI & Machine Learning Blog</h1>

<p class="hero-subtitle">
Insights on Machine Learning, Computer Vision, Deep Learning, research and real-world experience.
</p>
<p style="display:none;">
machine learning blog, computer vision blog, deep learning articles, AI research notes, data science blog, artificial intelligence projects and insights
</p>

{% assign categories = site.posts | map: 'category' | uniq %}

{% for cat in categories %}
  <section class="category-block">
    <h2 class="category-title">
      {% if cat == "education" %} 🎓 Education
      {% elsif cat == "work" %} 💼 Work Experience
      {% elsif cat == "research" %} 🧠 Research
      {% else %} 🗂️ {{ cat | capitalize }}
      {% endif %}
    </h2>

    <ul class="post-list timeline">
      {% for post in site.posts %}
        {% if post.category == cat %}
          <li>
            <div class="post-card">
              <a class="post-link" href="{{ post.url | relative_url }}">
                {{ post.title }}
              </a>
              <span class="post-meta">{{ post.date | date: "%d %b %Y" }}</span>
            </div>
          </li>
        {% endif %}
      {% endfor %}
    </ul>
  </section>
{% endfor %}
