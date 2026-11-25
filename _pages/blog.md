---
title: "Blog"
layout: home
sidebar:
  nav: false
author_profile: false
---

## Recently Reviewed Works

{% assign reviewed = site.pages | where_exp: "p", "p.review_date" | sort: "review_date" | reverse %}
{% for p in reviewed limit: 10 %}
- [{{ p.title }}]({{ p.url }})
{% endfor %}
