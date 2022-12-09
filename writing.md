---
layout: default
title: Writing
rank: 4
---
## Writing

I have written a lot but saved very little. 

I am filling in this page in chronological order. The writing samples currently provided are not an accurate representation of my current style. 

Check out the [Blog](blog.html) for more informal writing. 

<p>
{% assign blog = site.html_pages | sort:"writing" | reverse %}
{% for item in blog %}
  {% if item.writing %}
	<h3><a href="{{ item.path | replace:'.md','.html' }}">{{ item.title }}</a>. <em>{{ item.date | date_to_string }}</em>.</h3> {{ item.excerpt }}
  {% endif %}
{% endfor %}
</p>