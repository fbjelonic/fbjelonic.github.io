---
title: "Favorite Places in the World"
permalink: /places/
layout: archive
---

<div class="entries-layout">
{% for place in site.places %}
  <div class="entry">
    <h2><a href="{{ place.url | relative_url }}">{{ place.title }}</a></h2>
    {% if place.excerpt %}
      <p class="entry-excerpt">{{ place.excerpt }}</p>
    {% endif %}
  </div>
{% endfor %}
</div>