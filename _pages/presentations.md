---
title: "Presentations"
layout: gridlay
excerpt: "Presentations"
sitemap: false
permalink: /presentations/
---

{% for talk in site.data.presentationlist %}

{% if talk.invited == 1 %} 
    {{ talk.title }}, presented by {{ talk.presenter }} at {{ talk.meeting }}, {{ talk.date }}, {{ talk.location }}. (Invited) 
{% endif %}

{% if talk.invited == 0 %} 
    {{ talk.title }}, presented by {{ talk.presenter }} at {{ talk.meeting }}, {{ talk.date }}, {{ talk.location }}. 
{% endif %}

{% endfor %}
