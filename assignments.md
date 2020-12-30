---
layout: page
title: Assignments
---

## Assignments

### Homework

{% assign hwbydue = site.hw | sort: "duedate" %}

{% for homework in hwbydue -%}

| [{{ homework.title }}]({{ homework.url | relative_url }}) | Due: {{ homework.duedate | date_to_string: "ordinal", "US"  }} |
{% endfor %}
