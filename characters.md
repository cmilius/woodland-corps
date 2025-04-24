---
layout: page
title: Characters
---

Welcome to the Woodland Corps character roster! Below is a list of our adventurers. Click on a name to learn more about their story.

{% for character in site.characters %}

{% if character.image %}  
![Prof Pic]({{ "assets/images/characters/" | append: character.image | relative_url }})
{% endif %}

# {{ character.title }}

##### {{ character.race }} | {{ character.class }}

[Read more...]({{ character.url | relative_url }})

---

{% endfor %}

