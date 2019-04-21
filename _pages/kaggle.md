---
layout: archive
title: "Kaggle"
permalink: /kaggle/
author_profile: True
header:
  image: "/images/icmc.jpg"

---

{% include base_path %}

{% assign order = site.kaggle | reverse %}

{% for post in order %}
  {% include archive-single.html %}
{% endfor %}
