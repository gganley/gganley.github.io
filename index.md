# This is a test

<ul class="posts">
{% for post in site.posts limit: 5 %}
  <div class="post_info">
    {{ post.content }}
  </div>
  {% endfor %}
</ul>