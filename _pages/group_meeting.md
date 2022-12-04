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


