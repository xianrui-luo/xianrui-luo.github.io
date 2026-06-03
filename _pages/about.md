---
permalink: /
title: ""
author_profile: false
classes: wide
redirect_from:
  - /about/
  - /about.html
---

{% assign featured_publications = site.publications | sort: 'date' | reverse %}

<div class="home-landing">
  <section class="home-hero">
    <div class="home-hero__profile">
      <img src="{{ '/images/profile.jpg' | relative_url }}" alt="Xianrui Luo portrait" class="home-hero__avatar">
      <div class="home-hero__links">
        <a href="mailto:{{ site.author.email }}">Email</a>
        <a href="mailto:{{ site.author.alternateemail }}">Alternate Email</a>
        <a href="{{ site.author.googlescholar }}">Google Scholar</a>
        <a href="https://github.com/{{ site.author.github }}">GitHub</a>
        <a href="{{ site.author.orcid }}">ORCID</a>
        <a href="{{ site.author.CV }}">CV</a>
      </div>
    </div>

    <div class="home-hero__content">
      <p class="home-hero__eyebrow">Xianrui (Eric) Luo</p>
      <h1 class="home-hero__title">Researcher in 3D Vision, Multi-Modal AI, and Construction Intelligence</h1>
      <p class="home-hero__subtitle">Shuimu Scholar (Postdoctoral Fellow), Institute of Future Cities and Infrastructures, Tsinghua University</p>
      <p class="home-hero__summary">I received my bachelor's degree in Automation and PhD in Artificial Intelligence from Huazhong University of Science and Technology. My work focuses on 3D vision, multi-modal learning, and construction automation, with recent projects spanning neural rendering, human modeling, and multimodal LLMs for safety-critical built environments.</p>

      <div class="home-pill-list">
        <span>3D Vision</span>
        <span>Neural Rendering</span>
        <span>Multi-Modal Learning</span>
        <span>Construction Automation</span>
      </div>
    </div>
  </section>

  <section class="home-section">
    <div class="home-section__header">
      <p class="home-section__eyebrow">Research Focus</p>
      <h2>Current Directions</h2>
    </div>
    <div class="home-grid home-grid--two">
      <div class="home-card">
        <h3>Multi-modal intelligence for construction</h3>
        <p>Building reliable multi-modal LLM systems for construction safety, scene understanding, and structured reasoning over visual and textual evidence.</p>
      </div>
      <div class="home-card">
        <h3>Human-centric 3D and neural rendering</h3>
        <p>Studying high-fidelity human avatar modeling, all-in-focus neural radiance fields, and practical capture pipelines for real-world scenes.</p>
      </div>
    </div>
  </section>

  <section class="home-section">
    <div class="home-section__header">
      <p class="home-section__eyebrow">Selected Work</p>
      <h2>Featured Publications</h2>
    </div>
    <div class="publication-highlight-list">
      {% for post in featured_publications limit:3 %}
        <article class="publication-highlight">
          <div class="publication-highlight__meta">
            <span>{{ post.date | date: "%Y" }}</span>
            {% if post.venue %}<span>{{ post.venue }}</span>{% endif %}
          </div>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          {% if post.author %}<p class="publication-highlight__authors">{{ post.author }}</p>{% endif %}
          <div class="publication-highlight__links">
            {% if post.paperurl %}<a href="{{ post.paperurl }}">Paper</a>{% endif %}
            {% if post.codeurl %}<a href="{{ post.codeurl }}">Code</a>{% endif %}
          </div>
        </article>
      {% endfor %}
    </div>
  </section>

  <section class="home-section home-section--timeline">
    <div class="home-section__header home-section__header--inline">
      <p class="home-section__eyebrow">Experience</p>
      <h2>Employment</h2>
    </div>

    <div class="experience-list">
      <article class="experience-item">
        <div class="experience-item__marker" aria-hidden="true"></div>
        <div class="experience-item__body">
          <div class="experience-item__topline">
            <h3>Postdoctoral Researcher | Institute of Future Cities and Infrastructures, Tsinghua University</h3>
            <p>Aug 2025 - Now</p>
          </div>
          <p>Advisor: <a href="https://www.civil.tsinghua.edu.cn/cmen/info/1092/1394.htm">Prof. Dongping Fang</a>. I lead a project on multi-modal LLMs in construction safety.</p>
        </div>
      </article>

      <article class="experience-item">
        <div class="experience-item__marker" aria-hidden="true"></div>
        <div class="experience-item__body">
          <div class="experience-item__topline">
            <h3>Project Officer | S-Lab for Advanced Intelligence, Nanyang Technological University</h3>
            <p>Nov 2023 - Nov 2024</p>
          </div>
          <p>Advisor: <a href="https://guosheng.github.io/">Prof. Guosheng Lin</a>. I lead a project on high-fidelity human avatar modeling.</p>
        </div>
      </article>
    </div>
  </section>

  <section class="home-section">
    <div class="home-section__header">
      <p class="home-section__eyebrow">Recent Updates</p>
      <h2>News</h2>
    </div>
    <div class="news-list">
      <div class="news-item"><span class="news-item__date">2025-11</span><p>Two papers accepted by AAAI 2026.</p></div>
      <div class="news-item"><span class="news-item__date">2025-02</span><p>One paper accepted by IEEE TPAMI 2025.</p></div>
      <div class="news-item"><span class="news-item__date">2024-11</span><p>One paper accepted by IEEE TPAMI 2024.</p></div>
      <div class="news-item"><span class="news-item__date">2024-07</span><p>One paper accepted by ECCV 2024.</p></div>
      <div class="news-item"><span class="news-item__date">2023-07</span><p>One paper accepted by ICCV 2023.</p></div>
      <div class="news-item"><span class="news-item__date">2023-06</span><p>Won Winner Award in NTIRE 2023 Bokeh Effect Transformation Challenge.</p></div>
    </div>
  </section>

  <section class="home-section">
    <div class="home-section__header">
      <p class="home-section__eyebrow">Community</p>
      <h2>Academic Service</h2>
    </div>
    <div class="home-grid home-grid--two">
      <div class="home-card">
        <h3>Conference Reviewer</h3>
        <p>CVPR, ICCV, ECCV, ACMMM, WACV</p>
      </div>
      <div class="home-card">
        <h3>Journal Reviewer</h3>
        <p>IEEE TCSVT, Automation in Construction</p>
      </div>
    </div>
  </section>
</div>
