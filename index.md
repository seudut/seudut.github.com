---
layout: index 
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}
<div class="row-fluid" style="padding-top:40px; padding-left:20px; padding-right:20px">
    <div class="posts" display="none"></div> 
  {% for post in site.posts limit:150 %}
        {% capture summary %}{{post.content | split:'<!--more-->' |first }}{% endcapture%}
    <div class="post row">
        <h3><a class="title" href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h3>
        <div>
          <cite style="font-size:11px">{{ post.date | date: "%Y-%m-%d" }}</cite> <i class="icon-tag"></i>  {% for tag in post.tags %}<a href="{{ BASE_PATH }}{{ site.JB.tags_path }}#{{ tag }}-ref">{{ tag }}</a>{% if forloop.last %}{% else %}, {% endif %}{% endfor %}
       </div> 
        <div class="post_at_index">
            {{post.excerpt}} 
        {% if post.excerpt != post.content %}<a href="{{ BASE_PATH }}{{ post.url }}" rel="nofollow" style="float:right; font-size:11px; margin-right:40px;">Read more...</a>{% endif %}
        </div>
        <div style="clear: both;"></div>
        <hr/>
    </div> 
 {% endfor %}
</div>
