---
layout: page
title: Français
lang: fr
permalink: /fr/
---
{% assign posts = site.posts | where: "lang", "fr" | reverse %}
{% assign seasons = posts | group_by: "season" %}
{% for s in seasons %}
  {% assign info = site.data.seasons[s.name].fr %}
  {% if info %}
  {% if site.data.seasons[s.name].banner %}
  <p><img src="{{ site.data.seasons[s.name].banner | relative_url }}" alt="{{ info.banner_alt | escape }}" style="max-width:100%;height:auto;"></p>
  {% endif %}
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
