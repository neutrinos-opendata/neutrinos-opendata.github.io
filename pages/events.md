---
permalink: /events.html
layout: default
title: CLARIPHY Events
---
<center> 
<h3> CLARIPHY Events</h3>
</center>

<br>
CLARIPHY team members are, or have been, involved in organizing the following events:

{% comment %}
Collect all events into a sortable array, then display in reverse chronological
order grouped by month. Years are derived dynamically from the data.
{% endcomment %}

{% assign all_events = "" | split: ',' %}
{% for event_hash in site.data.events %}
  {% assign all_events = all_events | push: event_hash[1] %}
{% endfor %}
{% assign all_events = all_events | sort: 'startdate' | reverse %}

{% assign current_month_key = "" %}
{% for event in all_events %}
{% assign month_key = event.startdate | date: "%Y-%m" %}
{% if month_key != current_month_key %}
{% unless current_month_key == "" %}</ul>{% endunless %}
{% assign current_month_key = month_key %}
<br>
<h5>{{ event.startdate | date: "%B, %Y" }}</h5>
<ul>
{% endif %}
<li>{{ event.startdate | date: "%-d %b" }}{{ event.enddate | date: " - %-d %b" }}, {{ event.startdate | date: "%Y" }} - <a href="{{ event.meetingurl }}">{{ event.name }}</a> (<i>{{ event.location }}</i>)</li>
{% endfor %}
{% if current_month_key != "" %}</ul>{% endif %}
<br>

