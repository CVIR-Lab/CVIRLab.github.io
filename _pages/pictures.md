---
title: "CVIR Lab - Pictures"
layout: piclay
excerpt: "CVIR Lab -- Pictures"
permalink: /pictures/
---

# Pictures
Jump to: [Journal Club](#journal-club), [Online Meetings](#online-meeting)


#### Gallery
(Right-click *'view image'* to see a larger image.)
{% assign number_printed = 0 %}
{% for pic in site.data.pictures_Leiden %}

{% assign even_odd = number_printed | modulo: 4 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-3 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/picpic/Gallery/{{ pic.image }}" class="img-responsive" width="95%" style="float: left" />
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd > 2 %}
</div>
{% endif %}


{% endfor %}

{% assign even_odd = number_printed | modulo: 4 %}
{% if even_odd == 1 %}
</div>
{% endif %}

{% if even_odd == 2 %}
</div>
{% endif %}

{% if even_odd == 3 %}
</div>
{% endif %}

<p> &nbsp; </p>

First advertisement.
<figure>
<img src="{{ site.url }}{{ site.baseurl }}/images/picpic/jc3.jpg" width="60%" >
</figure>


## Journal club
<figure>
<img src="{{ site.url }}{{ site.baseurl }}/images/picpic/jc1.jpg" width="60%">
</figure>

## On-meetings
<figure>
<img src="{{ site.url }}{{ site.baseurl }}/images/picpic/jc2.jpg" width="60%">
</figure>