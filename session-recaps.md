---
layout: page
title: Session Recaps
---

Welcome to the Woodland Corps session recaps! Below is a list of our recent adventures. Click on a recap to read more.

{% for recap in site.session-recaps reversed %}
# [{{ recap.title }}]({{ recap.url | relative_url }})
### {{ recap.date | date: "%B %d, %Y" }}
  {{ recap.content }}
{% endfor %}
