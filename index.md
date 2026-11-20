---
layout: default
lang: en
ref: home
permalink: /
---
<div class="home">
  <h1 style="font-style:italic;">Unlocking hidden pathways</h1>
  <p>Taking a subject from another angle, and leaving a few of our assumptions behind along the way. The conclusion is yours.</p>
  {% for line in site.data.lines %}
  {% assign l = line.en %}
  <section style="margin-top:2em;">
    <h2>{% if l.url %}<a href="{{ l.url | relative_url }}">{{ l.name }}</a>{% else %}{{ l.name }}{% endif %}</h2>
    <p>{{ l.description }}</p>
    {% if l.note %}<p><em>{{ l.note }}</em></p>{% endif %}
  </section>
  {% endfor %}
</div>
