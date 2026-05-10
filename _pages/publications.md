---
layout: single
title: "Publications"
permalink: /publications/
author_profile: true
---

See my [Google Scholar](https://scholar.google.com/citations?user=YPLnv_gAAAAJ&hl=en).

{% assign pubs = site.publications | sort: "date" | reverse %}
{% assign current_year = "" %}

{% for post in pubs %}
  {% assign year = post.date | date: "%Y" %}

  {% if year != current_year %}

## {{ year }}

  {% assign current_year = year %}
  {% endif %}

{{ post.content }}

{% endfor %}

