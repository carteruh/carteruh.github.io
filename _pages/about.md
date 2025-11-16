---
permalink: /
title: "Welcome to my homepage!"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

![Illustration of Robot interacting with Objects](/images/usingimitati.gif){: .align-right width="400px"}
Here are some quick facts about me:

🦾 My research interests are in **robotics** spanning **reasoning, policy learning, perception, and generative approaches**. 

🧑‍🎓 I recently graduated from the **University of Houston** with a B.S. in **Computer Science and Biomedical Engineering**.

🧑‍💻 I am a Research Intern at the **University of Washington** and full-time Engineer at **Microsoft**. 


## Overview
I am a Vietnamese-American born and raised in Houston, TX. I moved to Seattle after graduation to conduct my predoctoral research at the **University of Washington** in the **Robotics and State Estimation Lab** and **Personal Robotics Lab** advised by **Dieter Fox** (Founding Robotics Director at Ai2 and NVIDIA) and **Siddhartha Srinivasa** (Founding Robotics Director at Amazon Robotics AI, Partner at Madrona Ventures). My research investigates **robot manipulation** from the perspective of building action policies and robot learning systems centered on rich and diverse data representations for embodied reasoning such as task generalization and long-horizon planning. As a prospective doctoral student, I am deeply grateful to be supported by the **National Science Foundation** CISE Graduate Fellowship!

Outside of research, I am a software engineer at **Microsoft** building **Copilot** into **OneNote**.

Prior, I studied **Computer Science and Biomedical Engineering** focusing on **Machine Learning and Neural Engineering** throughout my bachelors at the **University of Houston**. During my bachelors, I spent four years working on a range of research topics (brain-machine interfaces, computer vision, and robotics). Notably, I spent over two years with **Dr. Shishir Shah** (Chief AI Officer at OU) developing pose-invariant methods for face recognition models (Bachelors Thesis, VISAPP 2025). 

For work experience, I have spent my past three summers interning at **Microsoft, Amazon Web Services, and Northrop Grumman** where I focused on engineering machine learning platforms and applying models for practical enterprise applications.

I always enjoy chatting so feel free to reach out at **carterung [at] gmail [dot] com**

## News
**August 2025** Selected as a 2025 National Science Foundation Computer and Information Science and Engineering Graduate Fellow! 

**July 2025** Released **RoboEval** -- exploring granular evaluation for bimanual manipulation

**February 2025** Published at the **20th International Conference on Computer Vision Theory and Applications (VISAPP) 2025** as **first-author**.
 
{% comment %} ---------- Publications ----------------------------------- {% endcomment %}
## 📝 Publications
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


  <!-- <td class="paper-thumb">
  <div class="thumb-wrap">
    {% if p.video %}
      <video muted loop playsinline preload="metadata">
        <source src="{{ p.video }}" type="images/mp4">
      </video>
    {% endif %}
    <img src="{{ p.thumb }}" alt="">
  </div>
  </td> -->


  <td class="paper-text">
      <span class="papertitle"><em>{{ p.title }}</em></span>
      <br>{{ p.authors | markdownify }}<br>
      <em>{{ p.venue }}</em><br>
      {% if p.links.paper %}<a href="{{ p.links.paper }}">paper</a>{% endif %}
      {% if p.links.project %}{% if p.links.paper %}/ {% endif %}<a href="{{ p.links.project }}">project page</a>{% endif %}
      {% if p.links.arxiv  %}{% if p.links.paper or p.links.project %}/ {% endif %}<a href="{{ p.links.arxiv  }}">arXiv</a>{% endif %}
      {% if p.links.code  %}{% if p.links.paper or p.links.project or p.links.arxiv %}/ {% endif %}<a href="{{ p.links.code }}">code</a>{% endif %}
      <p>{{ p.teaser | markdownify }}</p>
  </td>
  </tr>
  {% endfor %}
</table>


