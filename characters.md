---
layout: page
title: Characters
---

Welcome to the Woodland Corps character roster! Below is a list of our adventurers.

{% for character in site.characters %}

# {{ character.title }}

{% if character.profile-picture %}  
![Prof Pic]({{ character.profile-picture | relative_url }}){: style="max-width: 300px; max-height: 300px;" }
{% endif %}

##### {{ character.race | default: "Race" }} | {{ character.class | default: "Class" }}

{{ character.excerpt }}

[Read more...]({{ character.url | relative_url }})

---

{% endfor %}

