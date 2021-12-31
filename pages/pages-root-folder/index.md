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
---

Joe Gibbs Politz - <code>jpolitz@eng.ucsd.edu</code> -  [jpolitz.github.io](https://jpolitz.github.io)

## Material and Schedule

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

## Course Calendar

<iframe src="https://calendar.google.com/calendar/embed?src=c_qr732udb46jbievpbp102ekjmc%40group.calendar.google.com&ctz=America%2FLos_Angeles" style="border: 0" width="800" height="600" frameborder="0" scrolling="no"></iframe>

## Frequently Asked Questions

For now, this page is a placeholder and holds frequently asked questions about
the course. This site will switch to containing the official course website and
syllabus at the start of winter quarter (early January 2022).


**Q: Will the course have remote options?**

Currently, I'm not planning any remote or asynchronous options for CSE 15L
beyond the first two weeks.  You should make sure you're available at the times
and places listed on the course schedule.

It's helpful to me if you let me know (<code>jpolitz@eng.ucsd.edu</code>) if
you would like a remote/asynchronous option and why.

**Q: I have a question about enrollments, section times, or the waitlist.**

Reach out to the folks at CSE student affairs:

[https://cse.ucsd.edu/undergraduate/advising/cse-student-affairs-office-hours](https://cse.ucsd.edu/undergraduate/advising/cse-student-affairs-office-hours)

They know much more than me about timelines, waitlist logistics, policies for
majors and non-majors enrollment, and so on.

