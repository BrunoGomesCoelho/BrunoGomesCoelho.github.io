---
layout: single
classes: wide
title: "Research"
permalink: /research/
author_profile: True
# header:
#   image: "/images/icmc.jpg"

---

{% include base_path %}

See also my [Google Scholar](https://scholar.google.com/citations?user=xu1_CAUAAAAJ). Below recent publications:


- [Understanding Inequality of LLM Fact-Checking over Geographic Regions with Agent and Retrieval models](https://arxiv.org/abs/2503.22877)
	- ***Bruno Coelho***, Shujaat Mirza, Yuyuan Cui, Christina Pöpper, Damon McCoy

- [Global-Liar: Factuality of LLMs over Time and Geographic Regions](https://arxiv.org/abs/2401.17839)
	- Shujaat Mirza, ***Bruno Coelho***, Yuyuan Cui, Christina Pöpper, Damon McCoy

- [Propaganda Política Pagada: Exploring U.S. Political Facebook Ads en Español]({{ site.baseurl }}{% link download/spanish-ads-www2023.pdf %}) 
	- ***Bruno Coelho***, Tobias Lauinger, Laura Edelson, Ian Goldstein, Damon McCcoy 
	- Presented at the [2023 ACM Web Conference (WWW 2023)](https://www2023.thewebconf.org/) in May 2023. / [doi](https://doi.org/10.1145/3543507.3583425)
	- For supplementary material, see [here]({% link _research/2023-05-01-spanish-ads-www.md %})

- [Optimal Team Economic Decisions in Counter-Strike](https://arxiv.org/abs/2109.12990)
	- Peter Xenopoulos, ***Bruno Coelho***, Claudio Silva
	- AISA-2021 

### Other research projects I've been a part of:
- NE-Motion: Visual Analysis of Stroke Patients Using Motion Sensor Networks 
	- RC Contreras, A Parnandi, ***BG Coelho***, C Silva, H Schambra, LG Nonato 
	- Sensors 2021 / [doi](https://doi.org/10.3390/s21134482)

- A new multi-filter framework with statistical dense SIFT descriptor for spoofing detection in fingerprint authentication systems 
	- Rodrigo Colnago Contreras, Luis Gustavo Nonato, Maurílio Boaventura, Inês Aparecida Gasparotto Boaventura, ***Bruno Gomes Coelho***, Monique Simplicio Viana 
	-  ICAISC 2021 / [doi](https://doi.org/10.1007/978-3-030-87897-9_39)

### Related blog posts:

{% assign order = site.research | reverse %}

{% for post in order %}
  {% include archive-single.html %}
{% endfor %}


