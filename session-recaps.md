---
layout: page
title: Session Recaps
---

After every session, our DM Next Door recounts the shenanigans that took place.  Click on a recap to read more and enjoy.

{% for recap in site.session-recaps reversed %}

{% if recap.image %}  
![Session Image]({{ recap.image | relative_url }})
{% endif %}

# {{ recap.title }}

##### {{ recap.date | date: "%B %d, %Y" }}

{{ recap.excerpt }}

[Read more...]({{ recap.url | relative_url }})

---

{% endfor %}
