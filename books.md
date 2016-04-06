---
layout: page
title : Readings
header : Book Readings
group: navigation
---
{% include JB/setup %}

<div class="readings">
  {% for post in site.posts %}
    {% if post.category == "reading" %}
      <article class="post">
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>

        <div class="entry">
          {{ post.content | truncatewords:10}}
        </div>

        <a href="{{ post.url }}" class="read-more">Read More >> </a>
      </article>
    {% endif %}
  {% endfor %}
</div>