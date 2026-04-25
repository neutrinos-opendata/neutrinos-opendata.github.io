---
permalink: /sitemap.html
layout: default
title: Sitemap
---
<h3>CLARIPHY Website Sitemap</h3>

{% comment %}
Go through the list of pages and create an index of them, separating by
different page categories (using our custom frontmatter tag "pagetype").
{% endcomment %}

<br>
<b>Project pages:</b>
<ul>
{% assign sorted = site.pages | sort_natural: 'title' %}
{% for mypage in sorted %}
  {% if mypage.layout == 'project' %} 
  <li><a href="{{mypage.permalink}}">{{ mypage.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

<br>
<b>Documentation pages:</b>
<ul>
{% assign sorted = site.pages | sort_natural: 'title' %}
{% for mypage in sorted %}
  {% if mypage.pagetype == 'doc' %} 
  <li><a href="{{mypage.permalink}}">{{ mypage.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

<br>
<b>Other pages:</b>
<ul>
{% assign sorted = site.pages | sort_natural: 'title' %}
{% for mypage in sorted %}
  {% if mypage.pagetype != 'doc' and mypage.pagetype != 'focus-area' and mypage.layout != 'project' and mypage.pagetype != 'fellow' and mypage.title %} 
  <li><a href="{{mypage.permalink}}">{{ mypage.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>


