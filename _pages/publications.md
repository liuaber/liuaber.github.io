---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

See my [Google Scholar](https://scholar.google.com/citations?user=YPLnv_gAAAAJ&hl=en).

{% assign pubs = site.publications | sort: "date" | reverse %}
{% assign current_year = "" %}

<div markdown="0">
{% for post in pubs %}
  {% assign year = post.date | date: "%Y" %}

  {% if year != current_year %}
    {% unless forloop.first %}</ul>{% endunless %}
    <h2>{{ year }}</h2>
    <ul>
    {% assign current_year = year %}
  {% endif %}

  <li>
    {{ post.content }}
  </li>

  {% if forloop.last %}</ul>{% endif %}
{% endfor %}
</div>
