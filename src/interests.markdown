---
title:  "My Many, Varied Interests"
---
<div>
  <a href="/">Home</a> > <a href="#0">Interests</a>
</div>
<div class="button-grid">
    {% for interest in site.interests %}
      {% assign path_parts = interest.relative_path | split: "/" %}
      {% if path_parts.size == 2 %}
        <a href="{{ interest.url }}" class="grid-btn">{{ interest.title }}</a>
      {% endif %}  
    {% endfor %}
</div>
