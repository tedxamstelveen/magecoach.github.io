{% assign posts = site.posts | sort: 'hits' %}
  {% for post in posts limit:4 %}
  <div class="col-1-4">
    <h3>{{ post.title }}</h3>
    <p>{{ post.intro }}</p>
    <p><a title="post.title" href="{{site.url}}{{ post.url }}">Lees meer...</a></p>
  </div>
{% endfor %}
