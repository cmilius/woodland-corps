---
layout: page
title: Characters
---

Welcome to the Woodland Corps character roster! Below is a list of our adventurers. Click on a name to learn more about their story.

{% for character in site.characters %}
- [{{ character.title }}]({{ character.url | relative_url }})
{% endfor %}
