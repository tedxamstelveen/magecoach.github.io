---
layout: default
title:
description:
keywords: 
nav: blog
---

# Blog


{% for post in site.posts %}

<amp-img noloading width="100" height="100" alt="{{ post.title }}" layout="responsive" src="{{site.static-url}}{{ post.image }}" class="photo pull-left"></amp-img>

## [{{ post.title }}]({{ site.baseurl }}{{ post.url }})

**{{ post.date | date: '%Y' }}-{{ post.date | date: '%m' }}-{{ post.date | date: '%d' }}** -
  {{ post.intro }}

  [>> Read more]({{site.baseurl}}{{ post.url }})



  * * *

{% endfor %}
