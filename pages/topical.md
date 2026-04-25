---
permalink: /topical.html
layout: default
title: CLARIPHY Topical Meetings
---
<center> 
<h3> CLARIPHY Topical Meetings</h3>
</center>

<br>
CLARIPHY topical meetings allow researchers in related areas to present
their work at all stages (early, in progress, post-publication) of their
efforts. We have a special focus on areas at the intersection of Physics
and Data Science, Machine Learning and Artificial Intelligence.
Zoom connections are always available and meetings are usually recorded.
Find all topical meeting agendas
[here](https://indico.fnal.gov/category/1253/).
<ul>

{% comment %}
Go through the list and produce a breakdown of the events in reverse 
chronological order, grouped by months
{% endcomment %}

{% include get_indico_list.html %}
{% assign selected_array = selected_array | reverse %}

{% assign hdrprint = "" %}
{% for event in selected_array %}
  {% assign eventyear = event.startdate | date: "%Y" %}
  {% assign eventmonth = event.startdate | date: "%m" %}
  {% assign newprint = event.startdate | date: "%B, %Y"%}
  {% if hdrprint != newprint %}
    {% if hdrprint != "" %}
      </ul>
    {% endif %}
    <br><h5>{{newprint}}</h5>
    <ul>
    {% assign hdrprint = newprint %}
  {% endif %}
  <li>{{event.startdate | date: "%-d %b" }}{{event.enddate | date: " - %-d %b" }}, {{event.startdate | date: "%Y" }} - <a href="{{event.meetingurl}}">{{event.name}}</a>
  {% if event.youtube.size > 4 %}
  - (<a href="{{event.youtube}}">Watch the meeting recording</a>)
  {% endif %}
  </li> 
{% endfor %}
</ul>
<br>

