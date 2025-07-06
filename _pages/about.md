---
permalink: /
title: "Welcome!"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

![Illustration of Robot interacting with Objects](/images/beemo.webp){: .align-right width="300px"}
Welcome to my homepage! Here are some quick facts about me:

🧑‍🎓 I recently graduated from the **University of Houston** with a B.S. in **Computer Science and Biomedical Engineering**.

🧑‍💻 I am a full-time Engineer at **Microsoft** and Research Intern at the **University of Washington**. 

📸 My research interests are in **embodied AI** spanning **computer vision, robotics, policy learning, perception, and generative approaches**. 

🦾 I am very passionate about leveraging AI and Computer Vision to applications in robotics, accessibility, and health.

## Overview
I am a Vietnamese-American born and raised in Houston, TX. I am currently at **Microsoft** working on enhancing **OneNote** for security and Copilot Notebook integration. 

I also am a research intern at the **University of Washington** in the **Robotics and State Estimation Lab** and **Personal Robotics Lab** advised by **Siddhartha Srinivasa** (UW) and **Dieter Fox** (NVIDIA). I actively investigate **robot learning** from the perspective of scaling simulation learning systems for policy learning in simulation and transferred to real-world robotic manipulation tasks.

I studied **Computer Science and Biomedical Engineering** focusing on **Machine Learning and Neural Engineering** throughout my bachelors at the **University of Houston**. During my bachelors, I spent three years working on a range of research topics (brain-machine interfaces, computer vision, and robotics). Notably, I spent over two years with **Dr. Shishir Shah** (University of Houston) developing pose-invariant methods for face recognition models (Bachelors Thesis, VISAPP 2025). 

For work experience, I have spent my past three summers interning at **Microsoft, Amazon Web Services, and Northrop Grumman** where I focused on engineering machine learning systems and applying models for practical enterprise applications.

May you have any questions or interest in collaboration please reach out to me at **carterung AT gmail.com**.

## News
**July 2025** Introducing my 2nd-author work **RoboEval** -- a structured evaluation framework for bimanual robot manipulation!

**February 2025** Published at the **20th International Conference on Computer Vision Theory and Applications (VISAPP) 2025** as **first-author**.

**November 2024** My research in pose-invariant face recognition was accepted and presented at the  **Rice Gulf Coast Undergraduate Research Symposium (GCURS) 2024** as an oral presentation.

 
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
      <a href="{{ p.links.paper }}">paper</a>
      {% if p.links.project %}/ <a href="{{ p.links.project }}">project page</a>{% endif %}
      {% if p.links.arxiv  %}/ <a href="{{ p.links.arxiv  }}">arXiv</a>{% endif %}
      {% if p.links.code  %}/ <a href="{{ p.links.code }}">code</a>{% endif %}
      <p>{{ p.teaser | markdownify }}</p>
  </td>
  </tr>
  {% endfor %}
</table>


