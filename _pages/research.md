---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

<style>
.paper {
  margin-bottom: 2em;
}
.paper-title {
  font-weight: bold;
  font-size: 1.1em;
}
.paper-meta {
  color: #666;
  margin: 0.2em 0;
}
.paper-venue {
  font-style: italic;
  margin: 0.2em 0;
}
details {
  margin-top: 0.5em;
}
details summary {
  cursor: pointer;
  color: #666;
  font-size: 0.95em;
  display: inline-block;
  list-style: none;
}
details summary::-webkit-details-marker {
  display: none;
}
details summary::before {
  content: '› ';
  font-size: 1.1em;
}
details[open] summary::before {
  content: '↓ ';
}
details summary:hover {
  color: #2c4a7c;
}
details p {
  margin-top: 0.5em;
  font-size: 0.95em;
  line-height: 1.6;
}
</style>

## Works in Progress

{% assign wips = site.publications | where: "category", "working_papers" | sort: "date" | reverse %}
{% for post in wips %}
<div class="paper">
  <div class="paper-title">
    {% if post.paperurl %}<a href="{{ post.paperurl }}">{{ post.title }}</a>{% else %}{{ post.title }}{% endif %}
  </div>
  <div class="paper-meta">{{ post.coauthors }}</div>
  <div class="paper-venue">{{ post.venue }}</div>
  {% if post.content and post.content != '' %}
  <details>
    <summary>Abstract</summary>
    <p>{{ post.content | strip_html | strip }}</p>
  </details>
  {% endif %}
  {% if post.fun_fact and post.fun_fact != '' %}
  <details>
    <summary>Dinner party fun fact</summary>
    <p>{{ post.fun_fact }}</p>
  </details>
  {% endif %}
</div>
{% endfor %}

---

## Publications

{% assign pubs = site.publications | where: "category", "publications" | sort: "date" | reverse %}
{% for post in pubs %}
<div class="paper">
  <div class="paper-title">
    {% if post.paperurl %}<a href="{{ post.paperurl }}">{{ post.title }}</a>{% else %}{{ post.title }}{% endif %}
  </div>
  <div class="paper-meta">{{ post.coauthors }}</div>
  <div class="paper-venue">{{ post.venue }}</div>
  {% if post.content and post.content != '' %}
  <details>
    <summary>Abstract</summary>
    <p>{{ post.content | strip_html | strip }}</p>
  </details>
  {% endif %}
  {% if post.fun_fact and post.fun_fact != '' %}
  <details>
    <summary>Dinner party fun fact</summary>
    <p>{{ post.fun_fact }}</p>
  </details>
  {% endif %}
</div>
{% endfor %}

---

## Graveyard

{% assign graveyard = site.publications | where: "category", "graveyard" | sort: "date" | reverse %}
{% for post in graveyard %}
<div class="paper">
  <div class="paper-title">
    {% if post.paperurl %}<a href="{{ post.paperurl }}">{{ post.title }}</a>{% else %}{{ post.title }}{% endif %}
  </div>
  <div class="paper-meta">{{ post.coauthors }}</div>
  <div class="paper-venue">{{ post.venue }}</div>
  {% if post.content and post.content != '' %}
  <details>
    <summary>Abstract</summary>
    <p>{{ post.content | strip_html | strip }}</p>
  </details>
  {% endif %}
  {% if post.fun_fact and post.fun_fact != '' %}
  <details>
    <summary>Dinner party fun fact</summary>
    <p>{{ post.fun_fact }}</p>
  </details>
  {% endif %}
</div>
{% endfor %}
