<hr>
{% assign posts = site.posts | sort: 'hits' %}
  {% for post in posts limit:2 %}
  <div class="col-1-2 red">
    <h3><a href="{{site.url}}{{post.url}}" title="{{ page.title }}">{{ post.title }}</a></h3>
    <p>{{ post.intro }}</p>
    <p><a title="post.title" href="{{site.url}}{{ post.url }}">» Lees meer</a></p>
  </div>
{% endfor %}
<hr>
