---
layout: page
title: Blog
group: navigation
description: Thinking Out Loud
feed: atom.xml
---


_Thinking Out Loud_ is [Girish Varma](/)'s personal blog 

More [information](info.html) about this blog, its [kith](kith.html) (blogroll, 
bookmarks, _etc._), and a complete archive of [past](past.html) posts, are 
available via links at the top of the page.

[![Feed icon](/files/css/feed-icon-14x14.png){:title="Atom feed of recent posts" .right}][feed]
A [feed][] of the most recent posts is also available.

[feed]: /iem/atom.xml

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

