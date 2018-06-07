---
title: TEDxAmstelveen Team leden
layout: default
description: Overzicht van alle team leden van TEDxAmstelveen.
keywords:
nav: team
image:
---

# Team

Het {{site.title}} evenement wordt georganiseerd door vrijwilligers uit Amstelveen en omstreken. Het evenement heeft geen commercieel, religieus of politiek doel. Het doel is om te inspireren, enthousiasmeren en verbinden. Wil jij meehelpen met {{site.title}} kijk dan [hier]({{site.url}}/jobs/) voor {{site.title}} vacatures.

<div class="tablet-up">
     <div class="card-container">
       {% for member in site.data.team %}
       {% if member.status == 'active' %}
       <div class="card">
         <div class="card__image">
           <a title="{{ member.name }}" href="{{ member.url }}">
           <amp-img
               noloading
               height="100"
               width="100"
               alt="{{ member.name }}"
               layout="responsive"
               src="/img/team/{{ member.pic }}.jpg">
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
     {% for member in site.data.team %}
     {% if member.status == 'active' %}
     <div class="card">
       <div class="card__image">
         <a title="{{ member.name }}" href="{{ member.url }}">
         <amp-img
             noloading
             height="200"
             width="200"
             alt="{{ member.name }}"
             layout="responsive"
             src="/img/team/{{ member.pic }}.jpg">
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
