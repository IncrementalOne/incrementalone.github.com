---
layout: latest-posts
---

<ul class="posts">
  {% for post in site.posts limit: 10 %}
      
      <h3 style="display:inline; margin-bottom:5px; margin-right:1.5em"><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h3>
      <h5 style="display:inline; margins:0"><span>{{ post.date | date_to_string }}</span><h5>
      <br>
      <div class="well">
      {{ post.content | strip_html | truncatewords:75}}
      </div>
      </br>
      {% endfor %}
</ul>
