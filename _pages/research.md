---
layout: archive
title: "Research"
permalink: /research/
author_profile: True
# header:
#   image: "/images/icmc.jpg"

---

{% include base_path %}

See my [Google Scholar](https://scholar.google.com/citations?user=xu1_CAUAAAAJ) for updated information; below some research projects:

Publications:
- Optimal Team Economic Decisions in Counter-Strike - Peter Xenopoulos, **Bruno Coelho** and Claudio Silva, AISA-2021 - Accepted, to-be published
- NE-Motion: Visual Analysis of Stroke Patients Using Motion Sensor Networks - RC Contreras, A Parnandi, **BG Coelho**, C Silva, H Schambra, LG Nonato - MDPI Sensors 2021 


{% assign order = site.research | reverse %}

{% for post in order %}
  {% include archive-single.html %}
{% endfor %}

