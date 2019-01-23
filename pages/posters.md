---
layout: page
show_meta: false
title: "Poster presentations"
header:
   image_fullwidth: "hawaiiMe.jpg"
permalink: "/presentations/posters/"
---
A common feature at physics conferences is the poster session, which give students and researchers the opportunity to present aspects of their work in detail. Interested colleagues discuss the posters with their presenters, typically over a glass of something and a tasty snack. Cheers to that! Here are some posters I've made.

{% assign sorted_talks = site.categories.posters | sort:date" | reverse %}

{% for talk in sorted_talks %}
<div class="row" markdown="1">
<div class="small-4 columns"><img src="../..{{talk.image}}"></div>
<div class="small-8 columns">
<a href="{{ talk.slides }}" target="_blank"> <strong>{{ talk.title }}</strong></a>, presented {% if talk.with%} (with  {{talk.with}}){% endif %}  at <a href="{{talk.url}}" target="_blank">{{talk.conference}}</a>{% if talk.location %}, {{talk.location}}{% endif %}, {{ talk.date | date_to_long_string }}
{% if talk.proceedings %}  (<a href="{{talk.proceedings}}" target="_blank">Proceedings</a>) {% endif %}
</div>
</div>
<br/>
{% endfor %}


