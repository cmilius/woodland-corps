---
layout: page
title: Session Recaps
---

After every session, our DM Next Door recounts the shenanigans that took place.  Click on a recap to read more and enjoy.

{% for recap in site.session-recaps reversed %}
# [{{ recap.title }}]({{ recap.url | relative_url }})

{{ recap.content }}

---
##### {{ recap.date | date: "%B %d, %Y" }}\

{% endfor %}
