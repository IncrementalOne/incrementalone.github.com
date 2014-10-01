---
layout: latest-posts
---

<ul class="posts">
  {% for post in site.posts limit: 10 %}
      
      <h3 style="display:inline; margin-right:1.5em"><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h3>
      -
      <h3 style="display:inline"><span>{{ post.date | date_to_string }}</span></h3>
      <div class="well">
        {{ post.content | strip_html | truncatewords:75}}
      </div>
      <br><br>
      {% endfor %}
</ul>
