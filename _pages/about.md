---
permalink: /
title: ""
author_profile: false
redirect_from:
  - /about/
  - /about.html
---

{% include base_path %}

<div class="profile-header">
  <div class="profile-header__text">
    <h1 class="profile-header__name">Carter Ung</h1>
    <p class="profile-header__title">Incoming CS PhD at Johns Hopkins &middot; Embodied AI &amp; Robotics at University of Washington</p>
    <div class="profile-header__links">
      <a href="mailto:carterung@gmail.com"><i class="fas fa-fw fa-envelope"></i> Email</a>
      <a href="{{ site.author.CV }}"><i class="fas fa-fw fa-file-lines"></i> CV</a>
      <a href="{{ site.author.googlescholar }}"><i class="fas fa-fw fa-graduation-cap"></i> Scholar</a>
      <a href="https://github.com/{{ site.author.github }}"><i class="fab fa-fw fa-github"></i> GitHub</a>
      <a href="https://www.linkedin.com/in/{{ site.author.linkedin }}"><i class="fab fa-fw fa-linkedin"></i> LinkedIn</a>
    </div>
  </div>
  <div class="profile-header__photo">
    <img src="{{ base_path }}/images/{{ site.author.avatar }}" alt="{{ site.author.name }}">
  </div>
</div>

I am an incoming CS PhD student at **The Johns Hopkins University**, advised by <a href="https://homangab.github.io/">**Homanga Bharadhwaj**</a> (Research Scientist, <a href="https://about.meta.com/realitylabs/">Meta Reality Labs</a>) and <a href="https://www.cs.jhu.edu/hager/">**Greg Hager**</a> (Director, <a href="https://www.nsf.gov/cise/">NSF CISE</a> and <a href="https://www.amazon.science/robotics">Amazon Robotics</a>). My research centers on **robot manipulation**: building action policies and learning systems that leverage rich, diverse data representations for embodied reasoning, task generalization, and long-horizon planning. I am supported by the **NSF CISE Graduate Fellowship**.

Currently, I am a predoctoral researcher at the **University of Washington**, advised by <a href="https://homes.cs.washington.edu/~fox/">**Dieter Fox**</a> (Sr. Director, <a href="https://allenai.org/">Ai2</a>) and <a href="https://goodrobot.ai/">**Siddhartha Srinivasa**</a> (Partner, <a href="https://www.madrona.com/">Madrona Ventures</a>) in the **Robotics and State Estimation Lab** and **Personal Robotics Lab**.

I also work as a software engineer at **Microsoft**, building **Copilot** into **OneNote**. Previously, I studied **Computer Science** and **Biomedical Engineering** at the **University of Houston**, where I spent over two years with **Dr. Shishir Shah** on pose-invariant face recognition (VISAPP 2025).

I've come across many kind people in my curious journey toward academia and industry. I am always open to chat and talk about perspectives in research, career, and life aspirations. Reach me at **carterung [at] gmail [dot] com**.

---

## News

**January 2026:** **RoboEval** accepted to **IEEE International Conference on Robotics and Automation (ICRA) 2026**!

**August 2025:** Selected as a 2025 **National Science Foundation Computer and Information Science and Engineering Graduate Fellow**!

---

## Publications

<table class="paper-grid">
  {% for p in site.data.papers %}
  <tr class="paper-row{% if p.highlight %} highlight{% endif %}">

    <td class="paper-thumb">
      <div class="paper-box-image">
        {% if p.video %}
          <video muted autoplay loop playsinline preload="metadata">
            <source src="{{ p.video | relative_url }}" type="video/mp4">
          </video>
        {% else %}
          <img src="{{ p.thumb | relative_url }}" alt="thumb">
        {% endif %}
      </div>
    </td>

    <td class="paper-text">
      <span class="papertitle">{{ p.title }}</span>
      <div class="paper-authors">{% if p.authors_html %}{{ p.authors_html }}{% else %}{{ p.authors | markdownify }}{% endif %}</div>
      <div class="paper-venue">{{ p.venue }}</div>
      <div class="paper-links">
        {% if p.links.project %}<a href="{{ p.links.project }}">Website</a>{% endif %}
        {% if p.links.paper %}<a href="{{ p.links.paper }}">PDF</a>{% endif %}
        {% if p.links.arxiv %}<a href="{{ p.links.arxiv }}">arXiv</a>{% endif %}
        {% if p.links.code %}<a href="{{ p.links.code }}">Code</a>{% endif %}
      </div>
      <p>{{ p.teaser | markdownify }}</p>
    </td>
  </tr>
  {% endfor %}
</table>
