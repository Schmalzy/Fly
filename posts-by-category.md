---
layout: page
title: "Posts by Category"
---

<section class="post-list">
{% for category in site.categories %}
    <h2 class="post-list-header">{{ category | first }}</h2>
    {% for posts in category %}
      {% for post in posts %}
        {% if post.title != "" %}
        <div class="post-list-item">
            <span class="post-list-date">{{ post.date | date: '%B %d, %Y' }}</span>
            <a class="post-list-link" href="{{ post.url }}">{{ post.title }}</a>
        </div>
        {% endif %}
      {% endfor %}
    {% endfor %}
{% endfor %}
</section>
<hr>
{% include intro.html %}