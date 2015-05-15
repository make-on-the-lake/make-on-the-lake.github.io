---
layout: default
title:  Welcome
---

# About Us

Make on the Lake is a maker group based in Cleveland Ohio.  We invite hobbyists,
makers, hackers, students, engineers, and anyone else who is into creating and
learning

Twice a month (on the first and fourth Thursday) we host an event.  Either a
guided workshop or a open hack night where you can work on any project you want.

Our guided workshops have an entry fee to pay for parts.  For details about
upcoming events checkout our page at [meetup.com](http://www.meetup.com/Make-on-the-Lake/).

{% assign most_recent_workshop = site.categories.workshop.first %}
{% assign post = most_recent_workshop %}

<h2><a href="{{ site.baseurl }}{{ most_recent_workshop.url }}">Most Recent Workshop: {{ most_recent_workshop.title }}</a></h2>
{% include post-meta.html %}
{{ most_recent_workshop.content }}

# Blog

{% for post in site.categories.post %}
  <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
  {% include post-meta.html %}
  {{ post.excerpt }}
{% endfor %}
