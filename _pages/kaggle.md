---
layout: archive
title: "Kaggle"
permalink: /kaggle/
author_profile: True
# header:
#   image: "/images/icmc.jpg"

---

During my undergraduate years I participated in various DS competions and hackatons. Here's a highlight of them:

{% include base_path %}

{% assign order = site.kaggle | reverse %}

{% for post in order %}
  {% include archive-single.html %}
{% endfor %}
