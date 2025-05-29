---
layout: page
title: Session Recaps
---


<link rel="stylesheet" href="{{ '/assets/css/main.css' | relative_url }}">

After every session, our DM Next Door recounts the shenanigans that took place.  Click on a recap to read more and enjoy.

{% for recap in site.session-recaps reversed %}

<div class="card">
{% if recap.image %}  
    <div class="card-image">
        <img src="{{ recap.image | relative_url }}" alt="RecapImg" />
    </div>
{% endif %}
    <div class="card-content">
        <h2><b>{{ recap.title }}</b></h2>
        <p><b>{{ recap.date | date: "%B %d, %Y" }}</b></p>
        <p>{{ recap.excerpt }}</p>
        <p><a href="{{ recap.url | relative_url }}">Read more...</a></p>
    </div>
</div>

{% unless forloop.last %}
---
{% endunless %}

{% endfor %}
