---
layout: default
title: "Characters"
---

# {{ page.title }}

Welcome to the Woodland Corps character roster! Below is a list of our adventurers. Click on a name to learn more about their story.

<ul>
{% for character in site.characters %}
  <li><a href="{{ character.url }}">{{ character.title }}{{site.characters}}</a></li>
{% endfor %}
</ul>