---
layout: archive
title: "Research"
permalink: /research/
author_profile: True
# header:
#   image: "/images/icmc.jpg"

---

{% include base_path %}

See my [Google Scholar](https://scholar.google.com/citations?user=xu1_CAUAAAAJ) for a list of recent publications, or below for older (pre PhD) projects:

{% assign order = site.research | reverse %}

{% for post in order %}
  {% include archive-single.html %}
{% endfor %}

