---
layout: page
title: English
lang: en
permalink: /
---
<ul class="post-list">
{% assign posts = site.posts | where: "lang", "en" %}
{% for post in posts reversed %}
  <li>
    <span class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
    <h3><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3>
  </li>
{% endfor %}
</ul>
