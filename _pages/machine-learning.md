---
layout: single
title: Machine Learning
permalink: /machine-learning/
---

<p>Exploring neural networks and optimization techniques.</p>

<ul>
  {% for post in site.categories.ML %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span style="color: #666; font-size: 0.85em"> — {{ post.date | date: "%Y-%m-%d" }}</span>
    </li>
  {% endfor %}
</ul>