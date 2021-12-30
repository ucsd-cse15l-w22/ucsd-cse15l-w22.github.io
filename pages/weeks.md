---
layout: page
show_meta: false
title: "Weekly Material"
subheadline: "Material for the course, organized by week"
header: no
permalink: "/weeks/"
---

<ul class="material">
    {% for post in site.categories.week reversed %}
    <li class="{% if post.current %}current{% endif %}">
    <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    <ul>
      {% for todo in post.todos %}
      <li><a href="{{ todo.url }}">{{ todo.name }}</a> - Due {{ todo.due-date }}</li>
      {% endfor %}
    </ul>
    
    </li>
    {% endfor %}
</ul>
