---
layout: page
permalink: home
title: home
---

**Categories**
{% for category in site.categories %}
- {{ category[0] }}
{% endfor %}

**Categories Posts**
{% for category in site.categories %}
- {{ category }}
{% endfor %}

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

**Notes:**
{% for post in site.categories.notes %}
{% if post.url %}
- {{ post.url }} {{ post.title }}
{% endif %}
{% endfor %}
