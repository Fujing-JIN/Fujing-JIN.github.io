---
layout: single
title: " "
permalink: /publications/
author_profile: true
---

<style>
  /* 强制隐藏整个页眉容器 */
  .page__header, .page__header-tabs, .page__title {
    display: none !important;
    visibility: hidden !important;
    height: 0 !important;
    margin: 0 !important;
    padding: 0 !important;
  }

  /* 移除主内容区域顶部的所有间距 */
  #main {
    margin-top: 0 !important;
    padding-top: 0 !important;
  }

  /* 针对内容包装器的极致压缩 */
  .page__inner-wrap {
    margin-top: 0 !important;
    padding-top: 0.5em !important; /* 留一点点呼吸感，如果想更紧凑可以改 0 */
  }

  /* 移除面包屑导航可能留下的空间 */
  .breadcrumbs {
    display: none !important;
  }
</style>

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
