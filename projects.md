---
layout: page
title: Projects
permalink: /projects/
---

Elenco sintetico di alcuni progetti. Per il codice vedi i link a GitHub.

<ul>
{% for p in site.data.projects %}
  <li>
    <strong><a href="{{ p.link }}">{{ p.name }}</a></strong> — {{ p.desc }}
    {% if p.tags %}<br><small>{{ p.tags | join: " · " }}</small>{% endif %}
  </li>
{% endfor %}
</ul>
