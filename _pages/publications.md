---
layout: archive
title: ""
permalink: /publications/
author_profile: true
---

{% include base_path %}

<style>
  /* 1. 彻底消除顶部空白 */
  .page__header, .page__title, .breadcrumbs { display: none !important; }
  #main { padding-top: 0 !important; margin-top: 0 !important; }
  .archive { margin-top: 0 !important; }

  /* 2. 标题间距优化 */
  h2 { margin-top: 1.2em !important; margin-bottom: 0.8em !important; border-bottom: 1px solid #eee; padding-bottom: 0.2em; }
  
  /* 3. 摘要折叠框样式：适配深色模式 */
  summary {
    color: inherit;
    font-weight: bold;
    cursor: pointer;
    margin-top: 0.5em;
    outline: none;
  }
  .abstract-text {
    margin-top: 10px;
    font-size: 0.95em;
    line-height: 1.5;
    color: inherit;
    text-align: justify;
    display: block;
  }
</style>

## Journal Articles / 期刊论文

{% for post in site.publications reversed %}
  {% if post.category == "manuscripts" %}
### [{{ post.title }}]({{ base_path }}{{ post.url }})
{{ post.citation }}

<details>
<summary>Abstract / 摘要 (点击展开)</summary>
<span class="abstract-text">{{ post.content | strip_html }}</span>
</details>
  {% endif %}
{% endfor %}

## Working Papers / 工作论文

{% for post in site.publications reversed %}
  {% if post.category == "working_papers" %}
### [{{ post.title }}]({{ base_path }}{{ post.url }})
{% if post.paperurl %}[[PDF Download]({{ post.paperurl }})]{% endif %}

<details>
<summary>Abstract / 摘要 (点击展开)</summary>
<span class="abstract-text">{{ post.content | strip_html }}</span>
</details>
  {% endif %}
{% endfor %}
