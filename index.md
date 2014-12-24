---
layout: latest-posts
---

<ul class="posts">
	{% for post in site.posts %}
		<h3 style="display:inline"> {{ post.title }} </h3>
		<h5 style="display:inline; margin-left:1em"> [ {{ post.date | date_to_string }} ] </h5>

		<div class="well" style="margin-top:6px">
			{{ post.excerpt }}
			<br>
			<a href="{{ BASE_PATH }}{{ post.url }}">Read more...</a>
		</div>
		<br>
	{% endfor %}
</ul>
