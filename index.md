---
layout: latest-posts
---

<ul class="posts">
  {% for post in site.posts limit: 10 %}
      <div class="well"></div>
      <h3 style="display:inline; margin-right:1.5em"><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h3>
      <h5 style="display:inline"><span>{{ post.date | date_to_string }}</span><h5>
      <br>
      {{ post.content | strip_html | truncatewords:75}}
      {% endfor %}
</ul>
