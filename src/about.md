---
layout: page
title: Articles
permalink: /about/
---

{% for post in site.posts %}
  * {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}

{% include google-analytics.html %}
