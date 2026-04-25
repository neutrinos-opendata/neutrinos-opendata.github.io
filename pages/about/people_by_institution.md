---
permalink: /about/people_by_institution.html
layout: people
title: CLARIPHY Collaboration
---

{% include institution_list.html %}

<div>
    {% for uniindex in institution_list %}
      {%- assign univ = site.data.universities[uniindex] -%}
      {%- assign active_count = 0 -%}
      {%- for memberid in univ.personnel -%}
        {%- assign member = site.data.people[memberid] -%}
        {%- if member.active and member.active == true -%}
          {%- assign active_count = active_count | plus: 1 -%}
        {%- endif -%}
      {%- endfor -%}
      {% if active_count > 0 %}
      <h5>{{univ.name}}</h5>
<div class="container pt-1 pb-3">
  <div class="row">
      {%- assign sorted_mapping = "" | split:"," -%}
      {%- for memberid in univ.personnel -%}
        {%- assign member = site.data.people[memberid] -%}
        {%- assign sortable_name = member.name | split:" " | reverse | join:" " -%}
        {%- capture item -%}
          {{sortable_name}};{{memberid}}
        {%- endcapture -%}
        {%- assign sorted_mapping = sorted_mapping | push: item -%}
      {%- endfor -%}
      {%- assign sorted_people = sorted_mapping | sort -%}

      {% for member in sorted_people %}
           {%- assign item = member | split:";" -%}
           {%- assign item = item[1] -%}
           {% assign person = site.data.people[item] %}
           {% if person.active and person.active == true %}
              {% include standard_person_card_2.md %}
           {% endif %}
      {% endfor %}
  </div>
</div>
      {% endif %}
    {% endfor %}
</div>

<!--
<div>
    <h2>The CLARIPHY Collaboration - Former Members</h2>
    {% for uniindex in institution_list %}
      {%- assign univ = site.data.universities[uniindex] -%}
      <h5>{{univ.name}}</h5>
<div class="container pt-1 pb-3">
  <div class="row">
      {%- assign sorted_mapping = "" | split:"," -%}
      {%- for memberid in univ.personnel -%}
        {%- assign member = site.data.people[memberid] -%}
        {%- assign sortable_name = member.name | split:" " | reverse | join:" " -%}
        {%- capture item -%}
          {{sortable_name}};{{memberid}}
        {%- endcapture -%}
        {%- assign sorted_mapping = sorted_mapping | push: item -%}
      {%- endfor -%}
      {%- assign sorted_people = sorted_mapping | sort -%}

      {% for member in sorted_people %}
           {%- assign item = member | split:";" -%}
           {%- assign item = item[1] -%}
           {% assign person = site.data.people[item] %}
           {% if person.active and person.active == true %}
           {% else %}
              {% include standard_person_card_2.md %}
           {% endif %}
      {% endfor %}
  </div>
</div>
    {% endfor %}
</div>
-->
