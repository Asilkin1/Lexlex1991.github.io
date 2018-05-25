---
layout: page
title: CIT237
permalink: /more/
---

<ul>
{% for post in site.faqs %} 
{% if post.categories contains "CIT237" %}
 <li>{{ post.title }}</li> 
{% endif %}
{% endfor %}
