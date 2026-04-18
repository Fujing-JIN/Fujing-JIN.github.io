---
layout: single
title: " "
permalink: /publications/
author_profile: true
---

<style>
  /* 1. 彻底隐藏页面顶部的标题区域及其占用的空间 */
  .page__header, .page__title {
    display: none !important;
  }
  /* 2. 压缩正文顶部多余的边距 */
  .page__inner-wrap {
    margin-top: 0 !important;
    padding-top: 0 !important;
  }
  /* 3. 针对 Academic Pages 这种特定的内容容器进行调整 */
  #main {
    padding-top: 1em !important;
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

## Working Papers / 工作论文
***

{% for post in site.publications reversed %}
  {% if post.category == "working_papers" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
