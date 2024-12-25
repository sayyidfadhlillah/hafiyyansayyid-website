---
title: "Student Supervision"
layout: gridlay
sitemap: false
permalink: /supervision/
---

## Alumni

<div class="jumbotron">
{% assign number_printed = 0 %}
{% for member in site.data.alumni %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}

<div class="row">
{% endif %}

<div class="col-sm-6 col-xs-12">
  <h4>{{ member.name }}</h4>
  <i>{{ member.duration }} <br> {{ member.info }}</i>
  <br>
  <br>
  Thesis title:
  <br>
  <br>
  {{member.thesis}}
  <ul style="overflow: hidden">
  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}

</div>
{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}

</div>
{% endif %}
</div>