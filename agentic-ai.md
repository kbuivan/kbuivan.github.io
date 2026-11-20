---
layout: page
title: Agentic AI
lang: en
ref: agentic-ai
permalink: /agentic-ai/
---
{% assign posts = site.posts | where: "lang", "en" | reverse %}
{% for entry in site.data.seasons %}
  {% assign key = entry[0] %}
  {% assign season = entry[1] %}
  {% assign info = season.en %}
  {% if season.banner %}
  <p><img src="{{ season.banner | relative_url }}" alt="{{ info.banner_alt | escape }}" style="max-width:100%;height:auto;"></p>
  {% endif %}
  <h2>{{ info.title }}</h2>
  {% if info.status %}<p><em>{{ info.status }}</em></p>{% endif %}
  <p>{{ info.description }}</p>
  {% assign items = posts | where: "season", key %}
  {% if items.size > 0 %}
  <ul class="post-list">
  {% for post in items %}
    <li><span class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
    <h3><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3></li>
  {% endfor %}
  </ul>
  {% endif %}
{% endfor %}
