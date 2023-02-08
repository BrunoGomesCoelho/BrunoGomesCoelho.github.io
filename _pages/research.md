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
- Propaganda Política Pagada: Exploring U.S. Political Facebook Ads en Español - **Bruno Coelho**, Tobias Lauinger, Laura Edelson, Ian Goldstein, Damon McCcoy - The Web Conference 2023 - Source will be available soon.
- Optimal Team Economic Decisions in Counter-Strike - Peter Xenopoulos, **Bruno Coelho** and Claudio Silva, AISA-2021 
- NE-Motion: Visual Analysis of Stroke Patients Using Motion Sensor Networks - RC Contreras, A Parnandi, **BG Coelho**, C Silva, H Schambra, LG Nonato - MDPI Sensors 2021 
- A new multi-filter framework with statistical dense SIFT descriptor for spoofing detection in fingerprint authentication systems - Rodrigo Colnago Contreras, Luis Gustavo Nonato, Maurílio Boaventura, Inês Aparecida Gasparotto Boaventura, **Bruno Gomes Coelho**, Monique Simplicio Viana -  ICAISC 2021


{% assign order = site.research | reverse %}

{% for post in order %}
  {% include archive-single.html %}
{% endfor %}

