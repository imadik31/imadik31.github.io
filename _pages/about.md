---
permalink: /
title: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi! I’m Madi Matymov, a PhD student in the Department of Statistics at KAUST (King Abdullah University of Science and Technology), where I am part of the [Bayesian Deep Learning group](https://bdl.kaust.edu.sa/) led by [Prof. Maurizio Filippone](https://mauriziofilippone.github.io/index.html).

My work lies at the intersection of Bayesian deep learning, data augmentation, and optimization in probabilistic models. My research examines how transformations and stochasticity influence generalization and how Bayesian principles can guide the design of more reliable and well‑calibrated deep learning systems.

My academic path naturally evolved from physics and applied mathematics toward statistical modeling. I completed my MS in Applied Mathematics at KAUST, where I analyzed wave scattering, transmission, and reflection in elastic plates, and applied deep learning models to study and predict these physical phenomena. This experience bridged classical wave physics and modern machine learning, forming a foundation for my current research on probabilistic modeling and robustness. Before that, I earned my BS in Mechanics from Gumilyov Eurasian National University (Kazakhstan), where I worked on the Tippe Top, studying its fascinating self‑inverting motion and dynamics.



## Latest News

<div class="latest-news">
{% assign items = site.data.news | sort: "date" | reverse %}
{% for n in items %}
  <div class="news-item">
    <div class="news-date">
      {{ n.date | date: "%B %d, %Y" }}{% if n.location %} {{ n.location }}{% endif %}
    </div>
    <p>
      {% if n.url %}
        {{ n.text | replace: "’","’" | replace: "‘","‘" | markdownify | strip_newlines }}
      {% else %}
        {{ n.text }}
      {% endif %}
    </p>
  </div>
{% endfor %}
</div>
