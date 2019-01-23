---
layout: page
show_meta: false
title: "Workshops"
header:
   image_fullwidth: "hawaiiMe.jpg"
permalink: "/presentations/workshops/"
---
I've taken part in some interesting workshops. Here are some of my contributions.

{% assign sorted_talks = site.categories.workshops | sort:date" | reverse %}

{% for talk in sorted_talks %}
<div class="row" markdown="1">
<div class="small-2 columns"><img src="../..{{talk.image}}"></div>
<div class="small-10 columns">
{% if talk.slides %}<a href="{{ talk.slides }}" target="_blank">{% endif %}  <strong>{{ talk.title }}</strong>{% if talk.slides %}</a>{% endif %} , presented  at <a href="{{talk.url}}" target="_blank">{{talk.conference}}</a>{% if talk.location %}, {{talk.location}}{% endif %} on {{ talk.date | date_to_long_string }}
</div>
</div>
<br/>
{% endfor %}


