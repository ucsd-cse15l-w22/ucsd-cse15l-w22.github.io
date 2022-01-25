---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: page-fullwidth
header: no

#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
title: "Software Tools & Techniques Lab (UCSD CSE15L)"
---

Joe Gibbs Politz - <code>jpolitz@eng.ucsd.edu</code> -  [jpolitz.github.io](https://jpolitz.github.io)

## Material and Schedule

<ul class="material">
    {% for post in site.categories.week reversed %}
    <li class="{% if post.current %}current{% else %}gray{% endif %}">
    <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    <ul>
      {% for todo in post.todos %}
      <li><a href="{{ todo.url }}">{{ todo.name }}</a> - Due {{ todo.due-date }}</li>
      {% endfor %}
    </ul>
    
    </li>
    {% endfor %}
</ul>

## Course Calendar

This calendar shows rooms for scheduled in-person lecture and lab meetings.

Visit Canvas to see Zoom links for remote sessions in the first two weeks.

<iframe src="https://calendar.google.com/calendar/embed?src=c_qr732udb46jbievpbp102ekjmc%40group.calendar.google.com&ctz=America%2FLos_Angeles&mode=WEEK" style="border: 0" width="800" height="600" frameborder="0" scrolling="no"></iframe>

## Frequently Asked Questions

For now, this page is a placeholder and holds frequently asked questions about
the course. This site will switch to containing the official course website and
syllabus at the start of winter quarter (early January 2022).


**Q: Will the course have remote options?**

Yes. The course will have remote lab options for the duration of the quarter.
There will be in-person lab options starting week 5.