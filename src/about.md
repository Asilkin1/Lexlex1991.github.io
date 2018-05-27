---
layout: page
title: All articles
permalink: /about/
---

{% for post in site.posts %}
  1. {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}

{% include google-analytics.html %}
