---
layout: latest-posts
---

<ul class="posts">
  {% for post in site.posts limit: 10 %}
      
      <h3 style="display:inline; margin:0; padding:0; line-height:2em">{{ post.title }}</h3>
      <h4 style="display:inline; margin:0; padding:0; line-height:2em; margin-left:1em"><span>[ {{ post.date | date_to_string }} ]</span></h4>
      <div class="well" style="margin-top:4px">
        {{ post.content | strip_html | truncatewords:75}}
        <br>
        <a href="{{ BASE_PATH }}{{ post.url }}">Read more...</a>
      </div>
      <br><br>
      {% endfor %}
</ul>
