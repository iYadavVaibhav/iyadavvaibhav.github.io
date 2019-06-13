---
layout: page
permalink: home
title: home
---

**Categories**
{% for category in site.categories %}
- {{ category[0] }}
{% endfor %}

## Archive

{% for category in site.categories %}
{% if category[0] != 'notes' %}
{% for post in category[1] %}
- [{{ post.title }}]({{ site.baseurl }}{{ post.url }}) under {{ post.categories }}, one {{ post.category }}
{% endfor %}
{% endif %}
{% endfor %}

**Notes:**
{% for post in site.categories.notes %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}

**Archives excludes notes**
{% for post in site.posts %}
{% unless post.categories contains 'notes' %}
- [{{ post.title }}]({{ post.url }})
{% endunless %}
{% endfor %}
