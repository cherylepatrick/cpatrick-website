---
layout: page
show_meta: false
title: "Conference talks"
header:
   image_fullwidth: "hawaiiMe.jpg"
permalink: "/presentations/talks/"
---
I've been lucky enough to travel to some fantastic places, and meet some amazing people, all in the name of neutrino physics! Take a look at the slides from some talks I've given to see the sorts of things we discuss at conferences.

{% assign sorted_talks = site.categories.talks | sort:date" | reverse %}

{% for talk in sorted_talks %}
<div class="row" markdown="1">
<div class="small-4 columns"><img src="../..{{talk.image}}"></div>
<div class="small-8 columns">
<a href="{{ talk.slides }}" target="_blank"> <strong>{{ talk.title }}</strong></a>, presented  at <a href="{{talk.exturl}}" target="_blank">{{talk.conference}}</a>{% if talk.location %}, {{talk.location}}{% endif %} on {{ talk.date | date_to_long_string }}
{% if talk.proceedings %}  (<a href="{{talk.proceedings}}" target="_blank">Proceedings</a>) {% endif %}
</div>
</div>
<br/>
{% endfor %}


