---
layout: archive
title: "Research"
permalink: /research/
author_profile: True
header:
  image: "/images/icmc.jpg"

---

{% include base_path %}


{% assign order = site.research | reverse %}

{% for post in order %}
  {% include archive-single.html %}
{% endfor %}
