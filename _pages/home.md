---
title: "Home"
layout: default
sitemap: false
permalink: /
---

<div id="homeid" class="col-sm-7 col-xs-12">

## Welcome!

<center>
<img src="{{ site.url }}{{ site.baseurl }}/images/teampic/group_2304.jpg" width="100%">
</center>
<p></p>
Welcome to our group's page! Feel free to take a look around. The site is still under construction; so check back for new content soon!

### ACME?!?
ACME stands for **A**ccelerated **C**omputation of **M**aterials for **E**nergy. The word "acme" also refers to "the point at which someone or something is best, perfect, or most successful," (per the OED) reminding us of what we can strive for in our work every day.

And finally, the ACME Corporation from Looney Tunes reminds us that while we set high standards for our research, we can't take ourselves too seriously all the time, and we always remember to find joy and laughter in work and life.

You can read more about our group's culture [here]({{ site.url }}{{ site.baseurl }}/values).

## Our Work
We are a computational materials science group in the Materials Science Department in the Carnegie Mellon School of Engineering, led by Prof. Rachel Kurchin. We focus on simulation and data-driven methods that can accelerate development and understanding of materials for a variety of clean energy applications, with a particular focus on ways we can use computation to maximize what we learn from experiments. Check out the [research page]({{ site.url }}{{ site.baseurl }}/research) for more!

</div>
<div id="newsid" class="col-sm-5 col-xs-12" >
<div>
{% for member in site.data.pi %}
<div class="jumbotron">
   <center>
<!-- <a href="{{site.url}}{{site.baseurl}}/team"><img src="{{site.url}}{{site.baseurl}}/images/teampic/{{ member.photo }}" width="50%" style="block:inline; margin-left:auto; margin-right:auto; margin-bottom:5px;"/></a> -->
   <h5>PI: {{ member.name }}</h5>
   <h6>{{ member.info1 }}</h6>
   <h7>{{ member.info2 }}</h7><br>
   <h7>{{ member.info3 }}</h7>
<div style="margin-bottom:5px">
   {% if member.twitter %}<a href="{{ member.twitter }}" target="_blank"><i class="fa fa-twitter-square fa-2x"></i></a> {% endif %}
   {% if member.cmu %}<a href="{{ member.cmu }}" target="_blank"><i class="ai ai-archive-square ai-2x"></i></a> {% endif %}
   {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-2x"></i></a> {% endif %}
   {% if member.cv %} <a href="{{ site.url }}{{ site.baseurl }}/{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-2x"></i></a> {% endif %}
   {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-2x"></i></a> {% endif %}
   {% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-2x"></i></a> {% endif %}
   {% if member.website %} <a href="{{ member.website }}" target="_blank"><i class="fa fa-external-link-square fa-2x"></i></a> {% endif %}
  </div>
  </center>
</div>
{% endfor %}
</div>

<div class="jumbotron">
<h2>News</h2>
  {% for article in site.data.news limit:7%}
  <b>{{ article.date }}</b>
    {{ article.headline }}
  {% endfor %}
  
  <h5><a href="{{ site.url }}{{ site.baseurl }}/allnews.html">... see all News</a></h5>
</div>
</div>
