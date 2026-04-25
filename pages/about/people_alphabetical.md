---
permalink: /about/people_alphabetical.html
layout: people
title: CLARIPHY Collaboration
---

{% include institution_list.html %}

{%- assign valid_people_ids = "" | split: "," -%}
{%- for uniindex in institution_list -%}
  {%- assign univ = site.data.universities[uniindex] -%}
  {%- for memberid in univ.personnel -%}
    {%- assign valid_people_ids = valid_people_ids | push: memberid -%}
  {%- endfor -%}
{%- endfor -%}

{%- assign sorted_mapping = "," | split:"," -%}
{%- for member in site.data.people -%}
  {%- assign sortable_name = member[1].name | split:" " | reverse | join:" " -%}
  {%- capture item -%}
    {{sortable_name}};{{member[0]}}
  {%- endcapture -%}
  {%- assign sorted_mapping = sorted_mapping | push: item -%}
{%- endfor -%}
{%- assign sorted_people = sorted_mapping | sort -%}

<div class="container-fluid">
<div class="row">
{% for member in sorted_people %}
  {%- assign pair = member | split:";" -%}
  {%- assign memberid = pair[1] -%}
  {%- if valid_people_ids contains memberid -%}
    {% assign person = site.data.people[memberid] %}
    {% if person.active and person.active == true %}
      {% include standard_person_card.md %}
    {% endif %}
  {% endif %}
{% endfor %}
</div>
</div>

