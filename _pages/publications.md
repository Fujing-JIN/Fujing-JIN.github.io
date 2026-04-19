---
layout: archive
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

<br>

## Working Papers / 工作论文
***

{% for post in site.publications reversed %}
  {% if post.category == "working_papers" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

<style>
  /* 强制消除 archive 布局可能残留的顶部微小间距 */
  .archive {
    margin-top: 0 !important;
  }
  .page__title {
    display: none !important;
  }
  #main {
    padding-top: 1em !important;
  }
</style>
