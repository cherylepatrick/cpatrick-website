---
layout: page
show_meta: false
title: "Publications"
header:
   image_fullwidth: "hawaiiMe.jpg"
permalink: "/research/publications/"
---

{% assign pubs_by_date = site.categories.papers | sort:"date" | reverse %}
{% for pub in pubs_by_date %}
<p>{{pub.by}} <a href="http://dx.doi.org/{{ pub.doi }}" target="_blank"> <strong>{{ pub.title }}</strong></a><br/> <i>{{ pub.journal }}</i> {% if pub.arxiv %}<a href="https://arxiv.org/abs/{{pub.arxiv}}" target="_blank">(arXiv {{pub.arxiv}})</a>{% endif %}, {{ pub.date | date_to_long_string }}
{% endfor %}




