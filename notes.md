---
layout: page
title: Notes
permalink: /notes/
---

{% for post in site.posts %}
  <article>
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
    <!-- {{ post.excerpt }} -->
  </article>
{% endfor %}