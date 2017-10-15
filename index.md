# This is a test

{% for post in site.posts %}
  * [{{ post.title }}]({{ post.url }})
{% endfor %}
