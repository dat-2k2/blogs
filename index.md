---
layout: default
title: Home
---
# Latest Posts
{% for post in site.posts %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    {{ post.excerpt }}
  </article>
{% endfor %}