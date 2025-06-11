---
layout: page
title: Session Recaps
image_folder: "assets/images/session-recaps"
---

<link rel="stylesheet" href="{{ '/assets/css/main.css' | relative_url }}">

After every session, our DM Next Door recounts the shenanigans that took place.  Click on a recap to read more and enjoy.

{% for recap in site.session-recaps reversed %}

<div class="card">
    <div class="card-image">
        {% assign recap_name = recap.name | remove: '.md' %}
        {% assign image_files = site.static_files | where_exp: "file", "file.path contains site.data.config.session_recap_image_directory" %}
        {% for img in image_files %}
            {% if img.path contains recap_name %}
                <img src="{{ img.path | relative_url }}" alt="RecapImg" />
            {% endif %}
        {% endfor %}
    </div>

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
