---
layout: default
title: Home
---

<div class="home">
    <h1 class="page-heading">{{ page.title }}</h1>
    <hr>
    {%- if site.posts.size > 0 -%}
        {%- for post in site.posts -%}
            <h3>
                <a class="post-link" href="{{ post.url | relative_url }}">
                {{ post.title | escape }}
                </a>
            </h3>
            <div id="page-preview" style="margin-left: 5%">
                {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
                <span class="post-meta">{{ post.date | date: date_format }}</span>
                {{ post.excerpt }}
            </div>
            <hr>
        {%- endfor -%}
    {%- endif -%}
</div>
