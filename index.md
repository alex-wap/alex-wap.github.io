---
layout: page
title: Alex Wapniarski's Blog
tagline: 
---
{% include JB/setup %}

### About
Hi, my name is Alex. This is my [JekyllBootstrap](http://jekyllbootstrap.com/) blog. I studied Mechanical Engineering at Berkeley and now I work for Microsoft as a Software Developer. I attended and taught at [Coding Dojo](http://codingdojo.com) in Silicon Valley. My personal website is [alexw.tech](http://alexw.tech).

### Contact

Send me a short email at {mylastname}@gmail.com.

### Most Recent Post

<span>{{ site.posts[0].date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ site.posts[0].url }}">{{ site.posts[0].title }}</a>
{{ site.posts[0].excerpt}}
{{ site.posts[0].excerpt | markdownify }}


### Posts

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

<!-- ![ALT TEXT]({{ site.url }}/assets/images/IMAGE.jpg){: .img-responsive } -->



