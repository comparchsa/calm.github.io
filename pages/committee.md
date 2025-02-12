---
title: "Committee"
layout: default
categories: "navigation"
order: 6
---

# CALM Committee

<!-- NOTE: This page is automatically generated from _data/members.yml -->

<h3>Committee Members</h3>
<div class="member-profiles-grid">
{% for mem in site.data.members %}
{% if mem.category == 'committee-member' and mem.active %}
<a href="{{mem.website}}">
<div class="member-profile">
<div class="member-photo-container">
<img class="member-photo" src="{{ mem.photo | relative_url }}"/>
</div>
<div class="member-name">{{ mem.name }}</div>
</div>
</a>
{% endif %}
{% endfor %}
</div>

{% assign chairs = site.data.members
    | where_exp: "item", "item.category contains 'chair'"
    | where_exp: "item", "item.active"
%}

{% if chairs.size > 0 %}
<h3>Chairs</h3>
<div class="member-profiles-grid">
{% for mem in site.data.members %}
{% if mem.category == 'co-chairs' and mem.active %}
<a href="{{mem.website}}">
<div class="member-profile">
<img class="member-photo" src="{{ mem.photo | relative_url }}"/>
<div class="member-name">{{ mem.name }}</div>
</div>
</a>
{% endif %}
{% endfor %}
</div>
{% endif %}

<h3>Join us!</h3>

We are currently seeking CALM Committee members to help with the day-to-day
tasks of running a successful long-term mentoring program.  If you can commit
1-2 hours a week to a position that involves communicating with a wide swath of
members of the computer architecture community, please contact the chairs.
