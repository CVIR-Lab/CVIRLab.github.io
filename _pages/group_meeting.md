---
title: "Group meeting"
layout: textlay
excerpt: "Group meeting"
sitemap: false
permalink: /group_meeting/
---

## Group meeting and Journal Club Schedule

Group meetings are held every other week and journal club is held every week.

The normal time/place for Group meetings is Tues. 9:30-11:00 in 403 rom.

The normal time/place for Journal Club is Mon.9:30-11:30 in 709 rom

<b>Schedule is subject to change, please check frequently. </b>

<div class="row">
<div class="col-sm-6 clearfix">

### Group meeting

{% for meeting in site.data.seminar %}
  <b>{{ meeting.date}}</b>  {{ meeting.presenter}}
  <br /> 

{% endfor %}

</div>
  
<div class="col-sm-6 clearfix">
### Journal club
{% for journal in site.data.journal_club %}
  <b>{{ journal.date}}</b>  {{ journal.presenter}}
  <br /> 

{% endfor %}
</div>
</div>

## Pictures
Jump to: [Journal Club](#journal-club), [Online Meetings](#online-meetings)
(Right-click *'open image in new tab'* to see a larger image.)

#### Journal club
{% assign number_printed = 0 %}
{% for pic in site.data.pictures_journalclub %}

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


### Online meetings
{% assign number_printed = 0 %}
{% for pic in site.data.pictures_meetings %}

{% assign even_odd = number_printed | modulo: 4 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-3 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/picpic/Meetings/{{ pic.image }}" class="img-responsive" width="95%" style="float: left" />
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
