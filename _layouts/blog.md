{% include header.md %}
	<section class="content">
		{{ content }}
	</section>
	{% for post in site.posts %}
	<article class="posts">
		<h3><a href="{{post.url}}">{{ post.title }}</a></h3>
		<span class="date">{{ post.date | date: "%-d %B %Y %-H:%M" }}</span>
		<p><a href="{{post.url}}" class="invisible">{{ post.content | replace: '\n',' ' |strip_html | truncatewords: 50 }}</a></p>
	</article>
{% endfor %}
{% include footer.md %}
