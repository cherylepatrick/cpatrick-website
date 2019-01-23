---
layout: page
show_meta: false
title: "Seminars"
header:
   image_fullwidth: "hawaiiMe.jpg"
permalink: "/presentations/seminars/"
---
One of the best parts of being a physicist is meeting fellow researchers from around the world and being able to share the research everyone is doing. One of the best ways to do that is by giving seminars at other universities and labs. I've been fortunate enough to be invited to speak at some great places, and to meet really interesting people. Here are some of the talks I've given.

{% assign sorted_talks = site.categories.seminars | sort:date" | reverse %}

{% for talk in sorted_talks %}
<div class="row" markdown="1">
<div class="small-2 columns"><img src="../..{{talk.image}}"></div>
<div class="small-10 columns">
{% if talk.slides %}<a href="{{ talk.slides }}" target="_blank">{% endif %}  <strong>{{ talk.title }}</strong>{% if talk.slides %}</a>{% endif %} , presented  at <a href="{{talk.url}}" target="_blank">{{talk.conference}}</a>{% if talk.location %}, {{talk.location}}{% endif %} on {{ talk.date | date_to_long_string }}
</div>
</div>
<br/>
{% endfor %}


