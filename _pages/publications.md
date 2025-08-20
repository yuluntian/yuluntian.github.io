---
layout: archive
title: "Featured Publications"
permalink: /publications/
author_profile: true
---

This page shows selected journal articles and conference papers.
For a complete list of my publications, please visit my [Google Scholar profile](https://scholar.google.com/citations?user=r-v0cusAAAAJ&hl=en&oi=ao) or see my [CV](/files/YulunTian_CV.pdf).

{% include base_path %}

{% assign show_preprints = false %}
{% if show_preprints %}
Preprints
------
{% endif %}
{% for post in site.publications reversed %}
  {% if post.status == "preprint" %}
    {% if post.include_on_website %}
      {% include publication-single.html %}
    {% endif %}
  {% endif %}
{% endfor %}

{% for post in site.publications reversed %}
  {% unless post.type contains "thesis" %}
    {% if post.include_on_website %}
      {% include publication-single.html %}
    {% endif %}
  {% endunless %}
{% endfor %}

<!-- Theses
======
{% for post in site.publications reversed %}
  {% if post.type contains "thesis" %}
    {% if post.include_on_website %}
      {% include publication-single.html %}
    {% endif %}
  {% endif %}
{% endfor %} -->
