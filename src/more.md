---
layout: page
title: CIT237
permalink: /more/
---

<ul>
{% for post in site.posts %} 
{% if post.categories contains "CIT237" %}
 <a href="#">post.title</a> 
{% endif %}
{% endfor %}
