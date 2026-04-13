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
      <a href="https://x.com/{{ site.author.twitter }}"><i class="fab fa-fw fa-x-twitter"></i> X</a>
    </div>
  </div>
  <div class="profile-header__photo">
    <img src="{{ base_path }}/images/{{ site.author.avatar }}" alt="{{ site.author.name }}">
  </div>
</div>

I am an incoming CS PhD student at **The Johns Hopkins University**, advised by <a href="https://homangab.github.io/">**Homanga Bharadhwaj**</a> (Research Scientist, <a href="https://about.meta.com/realitylabs/">Meta Reality Labs</a>) and <a href="https://www.cs.jhu.edu/hager/">**Greg Hager**</a> (Director, <a href="https://www.nsf.gov/cise/">NSF CISE</a> and <a href="https://www.amazon.science/robotics">Amazon Robotics</a>). My research is at the intersection of robotics and artificial intelligence: building full-stack robotic systems that can reason in clutter and operate in messy human environments. I am supported by the **NSF CISE Graduate Fellowship**.

Currently, I am a predoctoral researcher at the **University of Washington**, advised by <a href="https://homes.cs.washington.edu/~fox/">**Dieter Fox**</a> (Founding Director, <a href="https://research.nvidia.com/labs/srl/">Seattle NVIDIA Robotics Lab</a>) and <a href="https://goodrobot.ai/">**Siddhartha Srinivasa**</a> (Founding Director, <a href="https://www.amazon.science/robotics">Amazon Robotics AI</a>) in the **Robotics and State Estimation Lab** and **Personal Robotics Lab**.

I also work as a software engineer at **Microsoft**, building **Copilot** into **OneNote**. Previously, I studied **Computer Science** and **Biomedical Engineering** at the **University of Houston**, where I spent over two years with **Dr. Shishir Shah** on pose-invariant face recognition (VISAPP 2025).

I've come across many kind people in my curious journey toward academia and industry. I am always open to chat and talk about perspectives in research, career, and life aspirations. Reach me at **carterung [at] gmail [dot] com**.

---

<div class="research-statement" markdown="1">
*I work toward general-purpose robots that safely reason and manipulate alongside people in everyday environments.* I am interested in a) building full-stack robotic systems that continuously collect, train on, and evaluate diverse manipulation data with minimal expert involvement, b) learning generalizable representations from human data that capture how people reason, plan, and grasp across diverse tasks, and c) closing the loop between simulation and the real world for dexterous manipulation that continually grows skills through interaction and deployment.
</div>

---

## News

<ul class="news-list">
  <li><span class="news-date">Apr 2026</span> We release <a href="https://roboplayground.github.io/"><strong>RoboPlayground</strong></a> and partner with the <a href="https://x.com/BitRobotNetwork/status/2042244149135757591?s=20"><strong>BitRobot Network</strong></a> to unveil <strong>TeleArms</strong>!</li>
  <li><span class="news-date">Jan 2026</span> <a href="https://robo-eval.github.io"><strong>RoboEval</strong></a> accepted to <strong>IEEE International Conference on Robotics and Automation (ICRA) 2026</strong>!</li>
  <li><span class="news-date">Aug 2025</span> Selected as a 2025 <strong>National Science Foundation Computer and Information Science and Engineering Graduate Fellow</strong>!</li>
</ul>

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
