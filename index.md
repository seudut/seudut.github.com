---
layout: index 
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}
<div class="row-fluid" style="padding-top:40px">
<!--    <div class="post" display="none"></div> -->
  {% for post in site.posts limit:5 %}
        {% capture summary %}{{post.content | split:'<!--more-->' |first }}{% endcapture%}
    <div class="post row">
        <h2><a class="title" href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
        <div class="post_at_index">
            {{summary}} 
        {% if summary != post.content %}<a href="{{ BASE_PATH }}{{ post.url }}" rel="nofollow">Read more...</a>{% endif %}
        </div>
        <br/>
        <div>
          <cite>{{ post.date | date: "%Y-%m-%d" }}</cite> <i class="icon-tag"></i>  {% for tag in post.tags %}<a href="{{ BASE_PATH }}{{ site.JB.tags_path }}#{{ tag }}-ref">{{ tag }}</a>{% if forloop.last %}{% else %}, {% endif %}{% endfor %}
       </div> 
        <div style="clear: both;"></div>
        <hr/>
    </div> 
 {% endfor %}
</div>
<!--
-->

<!--
refert http://jolestar.com/

Read [Jekyll Quick Start](http://jekyllbootstrap.com/usage/jekyll-quick-start.html)

Complete usage and documentation available at: [Jekyll Bootstrap](http://jekyllbootstrap.com)

## Update Author Attributes

In `_config.yml` remember to specify your own data:
    
    title : My Blog =)
    
    author :
      name : Name Lastname
      email : blah@email.test
      github : username
      twitter : username

The theme should reference these variables whenever needed.
    
## Sample Posts

This blog contains sample posts which help stage pages and blog data.
When you don't need the samples anymore just delete the `_posts/core-samples` folder.

    $ rm -rf _posts/core-samples

Here's a sample "posts list".

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## To-Do

This theme is still unfinished. If you'd like to be added as a contributor, [please fork](http://github.com/plusjade/jekyll-bootstrap)!
We need to clean up the themes, make theme usage guides with theme-specific markup examples.

-->
