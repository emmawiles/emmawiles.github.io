---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

## Works in Progress

{% assign wips = site.publications | where: "category", "working_papers" | sort: "date" | reverse %}
{% for post in wips %}
  {% include archive-single.html %}
{% endfor %}

## Publications

{% assign pubs = site.publications | where: "category", "publications" | sort: "date" | reverse %}
{% for post in pubs %}
  {% include archive-single.html %}
{% endfor %}

## Graveyard

{% assign graveyard = site.publications | where: "category", "graveyard" | sort: "date" | reverse %}
{% for post in graveyard %}
  {% include archive-single.html %}
{% endfor %}
