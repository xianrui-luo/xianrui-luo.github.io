---
layout: archive
title: "Selected Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can find all of my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a> or <a href="{{site.author.CV}}">my CV</a>.</div>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
