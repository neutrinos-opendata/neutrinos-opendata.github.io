---
permalink: /collaborations.html
layout: default
title: Collaborations and Related Projects
---

# Collaborations and Related Projects

The CLARIPHY project and team members are part of a larger ecosystem of 
projects and collaborations focused on research on particle physics, data
science, artificial intelligence and cyberinfrastructure to support
science. These include:

{% for collab in site.data.collabcats %}
<br>
#### {{ collab.name }}
{%    for proj in site.data.collaborations[collab.id] %}
* [{{ proj.name }}]({{ proj.url }})
      {%- if proj.shortname -%}
          ({{ proj.shortname }})
      {%- endif -%}
      {%- if proj.description -%}
        : {{ proj.description }}
      {%- endif -%}
      {%- if proj.awards -%}
        {{ " -- " }}
        {%- assign awardlist = "" | split: "," -%}
        {%- for award in proj.awards -%}
           {%- capture awardtxt -%}
             [NSF&nbsp;{{award.type}}-{{award.number}}](https://www.nsf.gov/awardsearch/showAward?AWD_ID={{award.number}}&HistoricalAwards=false)
           {%- endcapture-%}
           {% assign awardlist = awardlist | push: awardtxt %}
        {%- endfor -%}
        {{ awardlist | join: ", " }}
    {%-  endif -%}
  {%- endfor %}
{% endfor %}
