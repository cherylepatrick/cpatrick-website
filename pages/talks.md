---
layout: page
show_meta: false
title: "Conference talks"
subheadline: "Scientific presentations I've given"
header:
   image_fullwidth: "hawaiiMe.jpg"
permalink: "/presentations/talks/"
---

{% assign sorted_talks = site.categories.talks | sort:date" | reverse %}

{% for talk in sorted_talks %}
<div class="row">
<div class="small-3 columns"><img src={{talk.image}}></div>
<div class=small-6 columns">
<a href="{{ talk.slides }}" target="_blank"> <strong>{{ talk.title }}</strong></a><br/>, presented  at <a href="{{talk.url}}" target="_blank">{{talk.conference}}</a>{% if talk.location %}, {{talk.location}}{% endif %}, {{ talk.date | date_to_long_string }}
{% if talk.proceedings %} <a href="{{talk.proceedings}}" target="_blank">Proceedings</a> {% endif %}
</div>
</div>
{% endfor %}


