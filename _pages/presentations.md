---
title: "CVIR Lab - Presentations"
layout: gridlay
excerpt: "CVIR Lab -- Presentations"
sitemap: false
permalink: /presentations/
---

{% for talk in site.data.presentationlist %}

{% if talk.invited_talk == 1 %} 
    {{ talk.title }}, presented by {{ talk.presenter }} at {{ talk.meeting }}, {{ talk.date }}, {{ talk.location }}. (Invited) 
{% endif %}


{% if talk.invited_talk == 0 %} 
    {{ talk.title }}, presented by {{ talk.presenter }} at {{ talk.meeting }}, {{ talk.date }}, {{ talk.location }}. 
{% endif %}

{% endfor %}
