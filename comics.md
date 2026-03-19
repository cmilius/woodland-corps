---
layout: page
title: Comics
image_folder: "assets/images/comics"
---

<link rel="stylesheet" href="{{ '/assets/css/main.css' | relative_url }}">

<div id="top-anchor"></div>

Our DM Next Door's talents are boundless. Here are some comical depictions of the shenanigans that took place.  Click on a comic and enjoy.

<a href="#bottom-anchor">Go to bottom ↓</a>

{% for comic in site.comics reversed %}
<!-- comic object fields you can use: -->
<!-- comic.title, comic.date, comic.excerpt, comic.url, comic.slug, comic.path, comic.id, comic.content, comic.categories, comic.tags, etc. -->
<!-- For the file name, use comic.path or comic.slug. comic.path gives the full path, comic.slug is usually the file name without extension. -->

<div class="card">
    <div class="card-image">
        {% assign comic_name = comic.path | split: '/' | last | split: '.' | first %}
        {% assign image_files = site.static_files | where_exp: "file", "file.path contains site.data.config.comics_image_directory" %}
        {% for comic_img in image_files %}
            {% assign filename = comic_img.path | split: '/' | last | split: '.' | first %}
            {% if filename == comic_name %}
                <img src="{{ comic_img.path | relative_url }}" alt="ComicImg" />
                {{ break }}
            {% endif %}
        {% endfor %}
    </div>

    <div class="card-content">
        <h2><b>{{ comic.title }}</b></h2>
        <p><b>{{ comic.date | date: "%B %d, %Y" }}</b></p>
        <p>{{ comic.excerpt }}</p>
        <p><a href="{{ comic.url | relative_url }}">Read more...</a></p>
    </div>
</div>

{% unless forloop.last %}
---
{% endunless %}

{% endfor %}

<a href="#top-anchor">Go to top ↑</a>

<div id="bottom-anchor"></div>