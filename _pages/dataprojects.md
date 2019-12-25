---
layout: archive
permalink: /data-projects/
title: "Data Science Posts"
author_profile: true
header:
  image: "/images/deltalab.jpg"
---

A portfolio of Data Science Projects

{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
