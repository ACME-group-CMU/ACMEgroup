---
title: "Team"
layout: gridlay
sitemap: false
permalink: /team/
---

## Team

 **We are looking for new group members!** [Read more here.]({{ site.url }}{{ site.baseurl }}/vacancies)


### PI

{% for member in site.data.pi %}
<div class="jumbotron">
<div class="row">
<div class="col-sm-2">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-9 col-xs-12">
  <h5>{{ member.name }}</h5>
  <h6>{{ member.info1 }}</h6>
<div class="row">
  * {{ member.info2 }}
  * {{ member.info3 }}
  </div>
{% if member.twitter %}<a href="{{ member.twitter }}" target="_blank"><i class="fa fa-twitter-square fa-2x"></i></a> {% endif %}
   {% if member.cmu %}<a href="{{ member.cmu }}" target="_blank"><i class="ai ai-archive-square ai-2x"></i></a> {% endif %}
   {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-2x"></i></a> {% endif %}
   {% if member.cv %} <a href="{{ site.url }}{{ site.baseurl }}/{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-2x"></i></a> {% endif %}
   {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-2x"></i></a> {% endif %}
   {% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-2x"></i></a> {% endif %}
   {% if member.website %} <a href="{{ member.website }}" target="_blank"><i class="fa fa-external-link-square fa-2x"></i></a> {% endif %}
</div>
</div>
</div>
{% endfor %}


### Members

<div class="jumbotron">

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-2 col-xs-12">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-4 col-xs-12">
  <h5>{{ member.name }}</h5>
  <h6><i>{{ member.info }}</i> 
  {% if member.coadvise %}(with {{member.coadvise}}){% endif %}<br></h6>
  {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-2x"></i></a> {% endif %}{% if member.website %} <a href="{{ member.website }}" target="_blank"><i class="fas fa-square-up-right fa-2x"></i></a> {% endif %} {% if member.cv %} <a href="{{ site.url }}{{ site.baseurl }}/{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-2x"></i></a> {% endif %} {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-2x"></i></a> {% endif %} {% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fab fa-github-square fa-2x"></i></a> {% endif %}{% if member.linkedin %} <a href="{{ member.linkedin }}" target="_blank"><i class="fa fa-linkedin-square fa-2x"></i></a> {% endif %}{% if member.researchgate %} <a href="{{ member.researchgate }}" target="_blank"><i class="ai ai-researchgate-square ai-2x"></i></a> {% endif %}{% if member.twitter %}<a href="{{ member.twitter }}" target="_blank"><i class="fa fa-twitter-square fa-2x"></i></a> {% endif %}
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

## Alumni

<div class="jumbotron">
{% assign number_printed = 0 %}
{% for member in site.data.alumni %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-2">
<img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-4 col-xs-12">
  <h4>{{ member.name }}</h4>
  {{member.duration}}<br>
  <i>{{ member.info }}</i>
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
<div style="text-align: center;">
  <a href="{{ site.url }}{{ site.baseurl }}/pets"><img src="{{ site.url }}{{ site.baseurl }}/images/cmu-scotty-scarf.png" width="100%" style="max-width:250px"/></a>
</div>
