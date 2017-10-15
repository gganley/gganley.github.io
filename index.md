<ul class="posts">
{% for post in site.posts limit: 5 %}
  <div class="post_info">
    {{ post.excerpt }}
    <a href="{{ site.url }}{{ post.url }}">Read more</a>
    </hr>
  </div>
  {% endfor %}
</ul>