---
layout: default
lang: fr
ref: home
permalink: /fr/
---
<div class="home">
  <h1 style="font-style:italic;" lang="en">Unlocking hidden pathways</h1>
  <p>Prendre un sujet par un autre angle, et laisser en chemin quelques-unes de nos idées reçues. La conclusion vous appartient.</p>
  {% for line in site.data.lines %}
  {% assign l = line.fr %}
  <section style="margin-top:2em;">
    <h2>{% if l.url %}<a href="{{ l.url | relative_url }}">{{ l.name }}</a>{% else %}{{ l.name }}{% endif %}</h2>
    <p>{{ l.description }}</p>
    {% if l.note %}<p><em>{{ l.note }}</em></p>{% endif %}
  </section>
  {% endfor %}
</div>
