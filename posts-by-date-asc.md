---
layout: page
title: "Start from the beginning"
---

<section class="post-list">
  {% assign posts_date = site.posts | sort %}
  {% for post in posts_date %}

    {% capture currentyear %}{{ post.date | date: "%Y" }}{% endcapture %}
    {% if currentyear != year %}
      <h2 class="post-list-header">{{ currentyear }}</h2>
      {% capture year %}{{ currentyear }}{% endcapture %}
    {% endif %}

    <div class="post-list-item">
        <span class="post-list-date">{{ post.date | date: '%B %d, %Y' }}</span>
        <a class="post-list-link" href="{{ post.url }}">{{ post.title }}</a>
    </div>

  {% endfor %}

</section>
<hr>
{% include intro.html %}