---
title: TEDxAmstelveen Talks
layout: default
description: Overzicht van alle talks van TEDxAmstelveen 2018.
keywords:
nav: talks
image:
---

# Talks

Op {{site.title}} 2018 stonden 9 sprekers op het podium met talks tussen 7 en 16 minuten. Er was een diversiteit zijn aan onderwerpen met aandacht voor onderwijs, zorg, muziek, techniek en natuurlijk Amstelveen. Hier een overzicht van alle talks van TEDxAmstelveen 2018.

<div class="tablet-up">
     <div class="card-container">
       {% for member in site.data.sprekers %}
       {% if member.status == 'active' %}
       <div class="card">
         <div class="card__image">

          {% if member.video != null %}         
            <amp-youtube height="240" layout="fixed-height" data-videoid="{{ member.video }}"> </amp-youtube>
          {% else %}
            <amp-img noloading height="400" width="400" alt="{{ member.name }}" layout="responsive" src="/img/sprekers/{{ member.pic }}.jpg"></amp-img>
          {% endif %}

         </div>
         <div class="card__content">
           <h3 class="card__title"><a title="{{ member.name }}" href="{{ member.url }}">{{ member.name }}</a></h3>
         </div>
       </div>
       {% endif %}
       {% endfor %}
     </div>
</div>

<amp-carousel class="tablet-down"
  width="auto"
  height="450"
  type="slides"
  layout="fixed-height">
  {% for member in site.data.sprekers %}
  {% if member.status == 'active' %}
  <div class="card">
    <div class="card__image">

      {% if member.video != null %}         
        <amp-youtube height="240" layout="fixed-height" data-videoid="{{ member.video }}"> </amp-youtube>
      {% else %}
        <amp-img noloading height="200" width="200" alt="{{ member.name }}" layout="responsive" src="/img/sprekers/{{ member.pic }}.jpg"></amp-img>
      {% endif %}

    </div>
    <div class="card__content">
      <h3 class="card__title"><a title="{{ member.name }}" href="{{ member.url }}">{{ member.name }}</a></h3>
    </div>

  </div>
{% endif %}
{% endfor %}
</amp-carousel>
