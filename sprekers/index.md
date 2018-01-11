---
title: TEDxAmstelveen Sprekers
layout: default
description: Overzicht van alle sprekers van TEDxAmstelveen.
keywords:
nav: sprekers
image:
---

# Sprekers

Op {{site.title}} 2018 zullen er 8 tot 10 sprekers zijn met talks tussen de 5 en 18 minuten. Er zal een diversiteit zijn aan onderwerpen met aandacht voor onderwijs, zorg, muziek, techniek en natuurlijk Amstelveen. Komende maanden zullen we langzaam onze sprekers bekend maken.

<div class="tablet-up">
     <div class="card-container">
       {% for member in site.data.sprekers %}
       {% if member.status == 'active' %}
       <div class="card">
         <div class="card__image">
           <a title="{{ member.name }}" href="{{ member.url }}">
           <amp-img
               noloading
               height="400"
               width="400"
               alt="{{ member.name }}"
               layout="responsive"
               src="/img/sprekers/{{ member.pic }}.jpg">
           </amp-img></a>
         </div>
         <div class="card__content">
           <h3 class="card__title"><a title="{{ member.name }}" href="{{ member.url }}">{{ member.name }}</a></h3>
           <p>{{ member.description }}</p>
         </div>
         <div class="card__action">
           <a title="{{ member.name }}" href="{{ member.url }}">Lees meer</a>
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
         <a title="{{ member.name }}" href="{{ member.url }}">
         <amp-img
             noloading
             height="400"
             width="400"
             alt="{{ member.name }}"
             layout="responsive"
             src="/img/sprekers/{{ member.pic }}.jpg">
         </amp-img></a>
       </div>
       <div class="card__content">
         <h3 class="card__title"><a title="{{ member.name }}" href="{{ member.url }}">{{ member.name }}</a></h3>
         <p>{{ member.description }}</p>
       </div>
       <div class="card__action">
         <a title="{{ member.name }}" href="{{ member.url }}">Lees meer</a>
       </div>
     </div>
   {% endif %}
   {% endfor %}
   </amp-carousel>
