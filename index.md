---
layout: page
title: English
lang: en
permalink: /
---
{% assign posts = site.posts | where: "lang", "en" | reverse %}
{% assign seasons = posts | group_by: "season" %}
{% for s in seasons %}
  {% assign info = site.data.seasons[s.name].en %}
  {% if info %}
  <h2>{{ info.title }}</h2>
  <p>{{ info.description }}</p>
  {% endif %}
  <ul class="post-list">
  {% for post in s.items %}
    <li><span class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
    <h3><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3></li>
  {% endfor %}
  </ul>
{% endfor %}

