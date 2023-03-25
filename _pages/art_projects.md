---
layout: archive
title: ""
permalink: /art/
author_profile: true
---

{% include base_path %}

{% for post in site.art_projects reversed %}
  {% include archive-single.html %}
{% endfor %}
