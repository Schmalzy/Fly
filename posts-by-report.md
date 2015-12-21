---
layout: page
title: "Fishing Reports"
---

<section class="post-list">
{% for post in site.categories.Reports %}
    <div class="post-list-item">
        <span class="post-list-date">{{ post.date | date: '%B %d, %Y' }}</span>
        <a class="post-list-link" href="{{ post.url }}">{{ post.title }}</a>
    </div>
{% endfor %}
</section>
<hr>
{% include intro.html %}