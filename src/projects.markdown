---
title:  "My Silly, Little Projects"
---
<div>
  <a href="/">Home</a> > <a href="#0">Projects</a>
</div>
<div class="button-grid">
    {% for project in site.projects %}
      {% assign path_parts = project.relative_path | split: "/" %}
      {% if path_parts.size == 2 %}
        <a href="{{ project.url }}" class="grid-btn">{{ project.title }}</a>
      {% endif %}  
    {% endfor %}
</div>

