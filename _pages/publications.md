---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<nav class="section-links" aria-label="Publication categories">
  <a href="#articles">Articles</a>
  <a href="#thesis">Ph.D. thesis</a>
  <a href="#patents">Patents</a>
</nav>

{% assign publications = site.publications | sort: 'date' | reverse %}

<h2 id="articles">Articles</h2>
{% for post in publications %}
  {% if post.publication_type == 'article' %}{% include publication-card.html %}{% endif %}
{% endfor %}

<h2 id="thesis">Ph.D. thesis</h2>
{% for post in publications %}
  {% if post.publication_type == 'thesis' %}{% include publication-card.html %}{% endif %}
{% endfor %}

<h2 id="patents">Patents</h2>
{% for post in publications %}
  {% if post.publication_type == 'patent' %}{% include publication-card.html %}{% endif %}
{% endfor %}
