---
layout: page
title: Characters
---

Welcome to the Woodland Corps character roster! Below is a list of our adventurers.

{% for character in site.characters %}

{% include character-card.html
    profile-picture=character.profile-picture
    name=character.title
    race=character.race
    class=character.class
    excerpt=character.excerpt
    url=character.url
%}

{% unless forloop.last %}
---
{% endunless %}

{% endfor %}
