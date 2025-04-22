---
layout: page
title: Session Recaps
---

# {{ page.title }}

Welcome to the Woodland Corps session recaps! Below is a list of our recent adventures. Click on a recap to read more.

{% for recap in site.session-recaps reversed %}
  {{ recap.date | date: "%B %d, %Y" }} - {{ recap.title }}
  {{ recap.content }}
{% endfor %}
