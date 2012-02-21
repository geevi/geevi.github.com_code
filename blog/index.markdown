---
layout: page
title: Blog
group: navigation
description: Thinking Out Loud
feed: atom.xml
---


_Thinking Out Loud_ is [Girish Varma](/)'s personal blog 

Recent Posts
------------

{% for post in site.categories.blog limit:5 %}

{{ post.date | date_to_string }}
**[{{ post.title }}]({{ post.url }})**
[View Comments]({{ post.url }}#disqus_thread) 

{{ post.excerpt }}

{% endfor %}

<p>
<a href="past.html">Older Posts &rarr;</a>
</p>

