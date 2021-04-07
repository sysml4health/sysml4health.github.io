---
layout: page
title: "Schedule"
---
{% include swc/schedule.html %}

{% comment %}
{% if site.carpentry == "swc" %}
{% include swc/schedule.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/schedule.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/schedule.html %}
{% endif %}
{% endcomment %}
