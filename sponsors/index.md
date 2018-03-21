---
title: TEDxAmstelveen Sponsors
layout: default
description: Overzicht van alle sponsoren van TEDxAmstelveen.
keywords:
nav: sponsors
image:
---

# Sponsor

Om het evenement toegankelijk en laagdrempelig te houden doen we een beroep op sponsoren om ons evenement kostendekkend uit te voeren. We zoeken zoveel mogelijk naar sponsoren in Amstelveen of met een verbinding met Amstelveen. We zoeken naar sponsoring in natura (barter) en sponsoring in geld. Wil je dit geweldige evenement steunen en sponsor worden neem dan contact op met [hallo@tedxamstelveen.com](mailto:hallo@tedxamstelveen.com?subject=Aanmelden {{site.title}} Sponsors)
<br><br>
TEDxAmstelveen 2018 werd mede mogelijk gemaakt door de geweldige hulp van:

<div class="tablet-up">
     <div class="card-container">
       {% for member in site.data.sponsors %}
       {% if member.status == 'active' %}
       <div class="card">
         <div class="card__image">
           <a title="{{ member.name }}" href="{{ member.url }}">
           <amp-img
               noloading
               height="200"
               width="600"
               alt="{{ member.name }}"
               layout="responsive"
               src="/img/sponsors/{{ member.pic }}.jpg">
           </amp-img></a>
         </div>
       </div>
       {% endif %}
       {% endfor %}
     </div>
</div>

<amp-carousel class="tablet-down"
  width="auto"
  height="250"
  type="slides"
  layout="fixed-height">
  {% for member in site.data.sponsors %}
  {% if member.status == 'active' %}
  <div class="card">
    <div class="card__image">
      <a title="{{ member.name }}" href="{{ member.url }}">
      <amp-img
          noloading
          height="200"
          width="400"
          alt="{{ member.name }}"
          layout="responsive"
          src="/img/sponsors/{{ member.pic }}.jpg">
      </amp-img></a>
    </div>
  </div>
{% endif %}
{% endfor %}
</amp-carousel>
