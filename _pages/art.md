---
layout: archive
title: "AI Art Projects and Residencies"
permalink: /art/
author_profile: true
---

{% include base_path %}

{% for post in site.art reversed %}
  {% include archive-single.html %}
{% endfor %}
