---
layout: page
permalink: home
title: home
---

## Archive


{% for category in site.categories %}
  {% if category[0] != 'notes' %}
    {% for post in category[1] %}
      - [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
    {% endfor %}
  {% endif %}
{% endfor %}

## Notes
{% for post in site.categories['notes'] %}
  - [{{ post.title }}]({{ post.url }})
{% endfor %}
