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
        {% assign recap_name = recap.slug %}
        {% assign image_files = site.static_files | where_exp: "file", "file.path contains site.data.config.session_recap_image_directory" %}
        {% for recap_img in image_files %}
            {% if recap_img.path contains recap_name %}
                <img src="{{ recap_img.path | relative_url }}" alt="RecapImg" />
                <p>{{ recap_img.path }} | {{ recap_name }} | End Test</p>
                {{ break }}
            {% endif %}
        {% endfor %}
        {% unless recap_name %}
        <!-- DEBUG: recap_name is blank for {{ recap.title }} -->
        {% endunless %}
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
