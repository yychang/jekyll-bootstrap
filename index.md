---
layout: default
---
 
{% for post in site.posts limit 4 %}
<span>{{ post.date | date_to_string }}</span> 
<h1><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h1>
{{ post.content }}
{% comment %} 
{{ post.content | strip_html | truncatewords:75}}<br> 
<a href="{{ post.url }}">Read more...</a><br><br>
{% endcomment %} 
{% endfor %}
