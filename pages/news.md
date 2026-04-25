---
permalink: /news.html
layout: default
title: "News, Featured Stories and Links"
---

<h1>News, Featured Stories and Links</h1>
{% for post in site.posts %}
  <div>
    <h4><a href="{{ post.url }}">{{ post.title }}</a></h4>
    <h6><i>{{ post.date | date_to_long_string }}</i></h6>
    {% if post.postimage %}
    <img src="{{post.postimage}}" class="float-start me-3 mb-2" style="width: 35%; max-width: 200px;">
    {% else %}
    <img src="/assets/images/Tprime-200pu-PhaseII-black-arctic-main-image-small.jpg" class="float-start me-3 mb-2" style="width: 10%">
    {% endif %}
    {% if post.summary %}
        {{ post.summary | markdownify }}
    {%- else %}
        {{ post.excerpt | strip_html }}
    {%- endif %}
    <div class="float-end">
    <a href="{{post.url}}">Read more</a>
    </div>
    <div class="clearfix"></div>
  </div>
  <hr>
{% endfor %}



*CLARIPHY is pleased to see our news stories reposted on the websites of other organizations. The stories should be reposted with credits to the CLARIPHY website and the original authors, as well as a link to the original posting. Any alterations to the text or images for the reposting should be agreed by the CLARIPHY Communications team.  Please email <mailto:owner@iris-hep.org>.*


