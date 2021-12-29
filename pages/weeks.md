---
layout: page
show_meta: false
title: "Weekly Material"
subheadline: "Material for the course, organized by week"
header: no
permalink: "/weeks/"
---
<ul>
    {% for post in site.categories.week %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>