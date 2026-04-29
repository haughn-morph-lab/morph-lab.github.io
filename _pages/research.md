---
title: "Research"
layout: single
permalink: /research/
toc: true
toc_label: "Projects"
toc_sticky: true
---

The MORPH Lab investigates why certain morphological designs produce superior maneuverability and adaptability — objectives that traditional optimization frameworks struggle to quantify. Drawing on principles observed across biological systems, we extract the design reasoning that governs the relationship between morphology, sensing, and control performance.

Our approach goes beyond traditional codesign. Rather than optimizing for well-defined metrics, we ask what morphological and sensory complexity is truly sufficient to meet a given performance objective — and why. The answers take the form of transferable design principles, validated through experimental prototypes.

Our work targets the next generation of agile robots — platforms capable of operating in complex, unpredictable environments where adaptability isn't a feature, it's a requirement. We believe better systems come from more than just better optimization, but from a deeper understanding of what good design actually means.

---

## Active Projects

{% assign sorted_projects = site.research | sort: "order" %}
{% for project in sorted_projects %}
### [{{ project.title }}]({{ project.url | relative_url }})

{{ project.excerpt | default: project.content | strip_html | truncatewords: 50 }}

{% if project.tags %}
**Keywords:** {{ project.tags | join: " · " }}
{% endif %}

---
{% endfor %}

{% if site.research.size == 0 %}
*Research project pages coming soon. Add files to `_research/` to populate this section.*
{% endif %}
