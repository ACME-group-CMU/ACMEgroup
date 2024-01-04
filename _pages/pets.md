---
title: "Pets"
layout: gridlay
sitemap: false
permalink: /pets/
---

## The Bestest Labmates


<div class="jumbotron">

{% assign number_printed = 0 %}
{% for member in site.data.pets %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-2 col-xs-12">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pets/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-4 col-xs-12">
  <h5>{{ member.name }}</h5>
  <h6><i>{{ member.info }}</i> </h6>
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

