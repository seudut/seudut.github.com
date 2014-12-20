---
layout: index 
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}
<div class="row-fluid" style="padding-top:40px; padding-left:20px; padding-right:20px">
    <div class="posts" display="none"></div> 
        <hr/>
  {% for post in site.posts limit:150 %}
        {% capture summary %}{{post.content | split:'<!--more-->' |first }}{% endcapture%}
    <div class="post row">
        <h3><a class="title" href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h3>
        <div>
          <cite style="font-size:11px; margin-left:10px; margin-right:10px; color:gray">{{ post.date | date: "Date: %b %d, %Y" }}</cite> <cite style="font-size:11px; margin-left:10px;color:gray">Tag:</cite><i class="icon-tag"></i>  {% for tag in post.tags %}<a href="{{ BASE_PATH }}{{ site.JB.tags_path }}#{{ tag }}-ref" style="font-size:11px">{{ tag }}</a>{% if forloop.last %}{% else %}<cite style="font-size:11px; color:gray">,</cite> {% endif %}{% endfor %}
       </div> 
        <div class="post_at_index" style="margin-top:9px">
            {{post.excerpt}} 
        {% if post.excerpt != post.content %}<a href="{{ BASE_PATH }}{{ post.url }}" rel="nofollow" style="float:right; font-size:11px; margin-right:40px; font-style:italic">Read more...</a>{% endif %}
        </div>
        <div style="clear: both;"></div>
        <hr/>
    </div> 
 {% endfor %}
</div>
