---
layout: page
subheadline: "CV"
title: "Cheryl's academic CV"
teaser: ""
header:
   image_fullwidth: "hawaiiMe.jpg"
permalink: "/cv/"
---
<ul>
    {% for post in site.tags.cv %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
