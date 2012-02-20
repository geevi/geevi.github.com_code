---
layout: page
title: "Articles & Talks"
group: navigation
---
{% include JB/setup %}


{% for post in site.categories.articles limit:5 %}

{{ post.date | date_to_string }}
**[{{ post.title }}]({{ post.url }})**
[View Comments]({{ post.url }}#disqus_thread) 

{{ post.excerpt }}

{% endfor %}
