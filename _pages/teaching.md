---
# layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: True
# header:
#   image: "/images/icmc.jpg"

---

{% include base_path %}

I am very passionate about teaching DS/ML/DL and have taken part in various projects:
- Co-founded [Data](http://data.icmc.usp.br/), a extracurricular DS group focused on teaching and developing DS projects at USP.
- Been a TA for the [Data Science MBA](http://cemeai.icmc.usp.br/MBA/) at USP since 2020 teaching Python, DS, ML and Deep Learning.
- Invited as a teacher at the [Python for Data Science course](https://www.icmc.usp.br/noticias/4503-icmc-oferece-curso-de-programacao-python-para-ciencia-de-dados)
- Headed the Data Science part of the Data Science and Engineering [course](https://www.sympla.com.br/trilha-de-data-scienceengineering__668265) at a startup incubator

With a focus on volunteering, I've also:

- Acted as a programming Tutor, teaching fundamentals of logic and computer programming to underprivileged communities
- Acted as a personal mentor to high school student, helped with doubts related to university life, building a study plan for the SATs and answering career questions.

See my [resume]({{ site.baseurl }}{% link download/Bruno_Gomes_Coelho_Resume.pdf %}) for a more detailed descriptions and relevant posts below:

{% assign order = site.teaching | reverse %}

{% for post in order %}
  {% include archive-single.html %}
{% endfor %}

