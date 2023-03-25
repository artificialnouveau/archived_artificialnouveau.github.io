---
layout: archive
title: "Art Projects and Residencies"
permalink: /art/
author_profile: true
---

{% include base_path %}

{% for post in site.art_projects %}
  {% include archive-single.html %}
{% endfor %}
