---
layout: page
title: "Articles & Talks"
group: navigation
---
{% include JB/setup %}

## Talks

[van Der Waerdern&#8217;s Theorem](http://girishvarma.wordpress.com/2009/03/14/van-der-waerdens-theorem/)  
Notes made for a student seminar at TIFR<

[Structure Theorem for Finitely Generated Modules](http://girishvarma.in/files/structure_theorem.pdf)  
Seminar given as a part of STCS Symposium.

## Academic Projects

[Approximate Counting, Almost Uniform Generation and Rapidly Mixing Markov Chains](http://db.tt/BZY0S96)  
Graduate project done under guidance of Manoj Gopalkrishnan [slides](http://db.tt/mOFYPvT)


[Pseudo-random Generators using the Directed Hamiltonian Path Problem](http://db.tt/1IWajMY)  
BTech major project done under guidance of [Dr. K. Muralikrishnan](http://nitc.ac.in/nitc/user_profile/index.jsp?__tg_login=kmurali)


[Parallelizing Algorithms for Molecular Dynamics Computations](http://db.tt/8Q0GbSY)  
BTech mini project done under guidance of [Vinod P](http://www.nitc.ac.in/nitc/user_profile/index.jsp?__tg_login=pathari)

[Microkernel Operating Systems](http://db.tt/MOx3MRC)  
BTech Seminar


{% for post in site.categories.articles limit:5 %}

{{ post.date | date_to_string }}
**[{{ post.title }}]({{ post.url }})**
[View Comments]({{ post.url }}#disqus_thread) 

{{ post.excerpt }}

{% endfor %}
