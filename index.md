---
layout: latest-posts
---

<ul class="posts">
  {% for post in site.posts limit: 10 %}
      
      <h3 style="display:inline; "><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h3>
      <h3 style="display:inline; margin:1em 0;"> - </h3>
      <h4 style="display:inline"><span>{{ post.date | date_to_string }}</span></h4>
      <div class="well" style="margin-top:4px">
        {{ post.content | strip_html | truncatewords:75}}
      </div>
      <br><br>
      {% endfor %}
</ul>
