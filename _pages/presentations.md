---
title: "CVIR Lab - Presentations"
layout: gridlay
excerpt: "CVIR Lab -- Presentations"
sitemap: false
permalink: /presentations/
---

{% assign number_printed = 0 %}
{% for talk in site.data.presentationlist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if talk.highlight == 1 %}


{% if even_odd == 0 %}
<div class="row">
{% endif %}


<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ talk.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/prepic/{{ talk.image }}" class="img-responsive" width="33%" style="float: left" />
  <p><em>presented by {{ talk.presenter }} at </em></p>
  <p class="text-danger"><strong> {{ talk.meeting}}</strong></p>
  <p><strong> {{ talk.date }}</strong></p>
  {% if talk.invited_talk == 1 %}
  <p> {{ talk.location }}.(Invited) </p>
  {% endif %}
  {% if talk.invited_talk == 0 %}
  <p> {{ talk.location }}. </p>
  {% endif %}
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>

## Full List of presentations

{% for talk in site.data.presentationlist %}

{% if talk.invited_talk == 1 %} 
    {{ talk.title }}, presented by {{ talk.presenter }} at {{ talk.meeting }}, {{ talk.date }}, {{ talk.location }}. (Invited) 
{% endif %}

{% if talk.invited_talk == 0 %}
    {{ talk.title }}, presented by {{ talk.presenter }} at {{ talk.meeting }}, {{ talk.date }}, {{ talk.location }}. 
{% endif %}

{% endfor %}