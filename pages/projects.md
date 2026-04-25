---
permalink: /projects.html
layout: default
title: CLARIPHY Projects
---

# Projects involving CLARIPHY collaborators

We list here a number of small projects which are underway and which involve CLARIPHY collaborators. These are often larger projects with additional participants, which can be found on the linked project pages.

<ul>
{% assign sorted = site.pages | sort_natural: 'title' %}
{% for mypage in sorted %}
{% if mypage.layout == 'project' %} 
  <li><a href="{{mypage.permalink}}">{{ mypage.title }}</a> - {{ mypage.description }} </li>
{% endif %}
{% endfor %}
</ul>
