---
layout: index 
title: Welcome
tagline: 
---

{% include JB/setup %}

这里是Payne的个人博客，用来记录工作，学习以及生活中的点点滴滴。

<hr>
<h4>Recent Articles</h4>
{% assign posts_collate = site.posts %}
<div id="home-article">
{% if site.JB.posts_collate.provider == "custom" %}
  {% include custom/posts_collate %}
{% else %}
  {% for post in posts_collate  %}
    {% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
    {% capture this_month %}{{ post.date | date: "%m" }}{% endcapture %}
    <li><p><span>{{ post.date | date: "%m/%e/%Y" }}</span> - <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></p></li>
  
  {% endfor %}
{% endif %}
{% assign posts_collate = nil %}
</div>

