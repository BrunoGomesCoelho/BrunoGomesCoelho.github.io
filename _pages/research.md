---
layout: archive
title: "Research"
permalink: /research/
author_profile: True
header:
  image: "/images/icmc.jpg"

---

{% include base_path %}


{% for post in site.research %}
  {% include archive-single.html %}
{% endfor %}
