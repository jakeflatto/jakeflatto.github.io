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
        <a href="{{ project.url | relative_url }}"
           class="grid-btn{% if project.image %} has-cover{% endif %}"
           {% if project.image %}style="--cover-img: url('{{ project.image | relative_url }}');"{% endif %}>
          <span class="grid-btn-label">{{ project.title | default: project.slug }}</span>
        </a>
      {% endif %}  
    {% endfor %}
</div>

