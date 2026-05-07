---
layout: archive
title: "Projects"
permalink: /projects/
description: "Selected robotics and software projects by Filip Bjelonic, from student-built platforms to exploratory control and autonomy experiments."
---

Here you can find a selection of projects I worked on as a student during my Bachelor and Master.

{% include base_path %}

{% assign sorted_projects = site.projects | sort: "date" | reverse %}
{% for post in sorted_projects %}
  {% include archive-single.html %}
{% endfor %}
