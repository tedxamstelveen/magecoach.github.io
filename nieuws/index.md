---
layout: default
title: TEDxAmstelveen laatste nieuws
description: Overzicht TEDxAmstelveen laatste nieuws.
keywords:
nav: nieuws
---
# Nieuws

{% for post in site.posts %}

<a href="{{site.url}}{{post.url}}" title="{{ page.title }}"><amp-img noloading width="100" height="100" alt="{{ post.title }}" layout="responsive" src="{{site.url}}{{ post.image }}" class="photo pull-left"></amp-img></a>

## [{{ post.title }}]({{ site.baseurl }}{{ post.url }})

**{{ post.date | date: '%Y' }}-{{ post.date | date: '%m' }}-{{ post.date | date: '%d' }}** -
  {{ post.intro }}

  [>> Lees meer]({{site.baseurl}}{{ post.url }})
  * * *

{% endfor %}
