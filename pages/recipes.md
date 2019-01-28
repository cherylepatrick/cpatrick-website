---
layout: page
show_meta: false
title: "Deliciousness"
header: no
permalink: "/recipes/"
teaser: "A girl's got to eat, and I choose to eat deliciously."
---

{% assign recipes = site.categories.recipes | sort:date" | reverse %}


{% for recipe in recipes %}
<div>
<h3>{{ recipe.title }}</h3>
<p><small>{{recipe.date | date: '%B %d, %Y'}}</small></p>
<img src="../images/recipes/{{ recipe.featured_image }}" alt="{{ recipe.title }}">

<p>{{ recipe.excerpt }}</p>

<p><a class="button" href="{{ recipe.url }}">Read more</a></p>
<hr/>
</div>
{% endfor %}

