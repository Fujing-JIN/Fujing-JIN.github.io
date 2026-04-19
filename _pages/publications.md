---
layout: archive
title: ""
permalink: /publications/
author_profile: true
---

{% include base_path %}

<style>
  /* 强制消除顶部所有占位空间 */
  #main { padding-top: 0 !important; margin-top: 0 !important; }
  .archive { margin-top: 0 !important; }
  /* 调整两个大标题之间的间距 */
  h2 { margin-top: 1.2em !important; margin-bottom: 0.8em !important; border-bottom: 1px solid #eee; padding-bottom: 0.2em; }
</style>

## Journal Articles / 期刊论文

{% for post in site.publications reversed %}
  {% if post.category == "manuscripts" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## Working Papers / 工作论文
***

{% for post in site.publications reversed %}
  {% if post.category == "working_papers" %}
### [{{ post.title }}]({{ post.url }})

{{ post.citation }} {% if post.paperurl %}[[PDF]({{ post.paperurl }})]{% endif %}

<details style="margin-top: 0.5em; cursor: pointer;">
  <summary style="color: #494E52; font-weight: bold;">Abstract / 摘要 (点击展开)</summary>
  <div style="margin-top: 10px; font-size: 0.95em; line-height: 1.5; color: #666; text-align: justify;">
    {{ post.content | strip_html }}
  </div>
</details>

<br />
  {% endif %}
{% endfor %}
