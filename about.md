---
layout: page
title: More
permalink: /about/
---

## All posts

{% for post in site.posts %}
  * {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}

{% include google-analytics.html %}
