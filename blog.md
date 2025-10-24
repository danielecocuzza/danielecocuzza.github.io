---
layout: page
title: 
permalink: /blog/
---
<h1 class="section-title">Blog</h1>

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
