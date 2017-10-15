<ul class="posts">
{% for post in site.posts limit: 5 %}
  <div class="post_info">
    {{ post.content }}
    [Read more]({{ post.url }})
  </div>
  {% endfor %}
</ul>