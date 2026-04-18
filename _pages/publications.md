---
layout: single
title: "Publications / 论文"
permalink: /publications/
author_profile: true
---

{% include base_path %}

## Journal Articles / 期刊论文
***

{% for post in site.publications reversed %}
  {% if post.category == "manuscripts" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

<br />

## Working Papers / 工作论文
***

{% for post in site.publications reversed %}
  {% if post.category == "working_papers" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
