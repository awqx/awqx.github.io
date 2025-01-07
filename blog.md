---
layout: default
title: Blog
rank: 3
---
## Blog

Cross-posted with Buttondown (eventually).

{% for post in site.posts %}
  <p>
  <a href="{{ post.url }}">{{ post.title }}</a>. ({{ post.words }} words). {{ post.date | date_to_string }}.
  <br>
  <small>{{ post.excerpt }}</small>
  </p>
{% endfor %}