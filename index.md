---
layout: page
---

<ul class="posts">
  {% for post in site.posts limit: 10 %}
      <h3 style="display:inline; margin-right:4em"><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h3>
      <h4 style="display:inline"><span>{{ post.date | date_to_string }}</span> &raquo;<h4>
      <br>
  {% endfor %}
</ul>
