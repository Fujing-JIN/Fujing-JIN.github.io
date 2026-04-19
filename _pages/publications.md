---
layout: archive
title: ""
permalink: /publications/
author_profile: true
---

{% include base_path %}

<style>
  /* 彻底消除顶部占位空间 */
  .page__header, .page__title, .breadcrumbs { display: none !important; }
  #main { padding-top: 0 !important; margin-top: 0 !important; }
  .archive { margin-top: 0 !important; }

  /* 调整标题间距 */
  h2 { margin-top: 1.2em !important; margin-bottom: 0.8em !important; border-bottom: 1px solid #eee; padding-bottom: 0.2em; }
  
  /* 列表项样式：仅保留标题链接 */
  .publication-list-item {
    margin-bottom: 0.8em;
    list-style: none;
  }
  .publication-title {
    font-size: 1.1em;
    font-weight: bold;
    text-decoration: none;
  }
</style>

## Journal Articles / 期刊论文

<ul style="margin-left: 0;">
{% for post in site.publications reversed %}
  {% if post.category == "manuscripts" %}
    <li class="publication-list-item">
      <a href="{{ base_path }}{{ post.url }}" class="publication-title">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>

## Working Papers / 工作论文

<ul style="margin-left: 0;">
{% for post in site.publications reversed %}
  {% if post.category == "working_papers" %}
    <li class="publication-list-item">
      <a href="{{ base_path }}{{ post.url }}" class="publication-title">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>
