---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

[Geometric Limits of Sums of Iterated and Fixed Polynomials](\files\KKW2024.pdf) (3.27 MB)<br>
&nbsp;&nbsp;&nbsp;&nbsp;Joint with A. Kapiamba and S. Kaschner, <br>
&nbsp;&nbsp;&nbsp;&nbsp;*submitted to* Ergodic Theory and Dynamical Systems, *fall 2024*.

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

<!-- New style rendering if publication categories are defined -->
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}