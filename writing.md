---
layout: default
title: Writing
rank: 4
---
## Writing

I have written a lot but saved very little. 

I am filling in this page in chronological order. The writing samples currently provided are not an accurate representation of my current style or current views. (The most accurate impression of my current views is probably going to be an in-person conversation, unfortunately). 

Check out the [Blog](blog.html) for more informal writing. 

{% assign blog = site.html_pages | sort:"writing" | reverse %}
{% for item in blog %}
  <p>
  {% if item.writing %}
	<b><a href="{{ item.path | replace:'.md','.html' }}">{{ item.title }}</a> ({{ post.words }} words). <em>{{ item.date | date_to_string }}</em>.</b> 
	<small>{{ item.excerpt }}</small>
	<br>
  {% endif %}
  </p>
{% endfor %}