---
layout: layout
title: Projects
---

{% for post in site.posts %}
    {% if post.category == 'projects' %}
        <div class="catalog-item">
            <a href="{{ post.url }}">
                {{ post.title }} ({{ post.date | date: "%Y" }})
                <img class="catalog-thumb" src="/images/thumbs/{{ post.title | slugify }}.jpg" alt="{{ post.title }}" />
            </a>
        </div>
    {% endif %}
{% endfor %}