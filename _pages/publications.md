---
layout: archive
title: ""
permalink: /publications/
author_profile: true
---

{% include base_path %}

<style>
  /* 1. 消除顶部及全局间距 */
  .page__header, .page__title, .breadcrumbs { display: none !important; }
  #main { padding-top: 0 !important; margin-top: 0 !important; }
  .archive { margin-top: 0 !important; }

  /* 2. 统一标题样式与间距 */
  h2 { margin-top: 1.2em !important; margin-bottom: 0.8em !important; border-bottom: 1px solid #eee; padding-bottom: 0.2em; }
  
  /* 3. 摘要折叠框样式优化：解决黑底看不清问题 */
  summary {
    color: inherit; /* 字体颜色跟随系统主题，适配深色模式 */
    font-weight: bold;
    cursor: pointer;
    margin-top: 0.5em;
    outline: none;
  }
  .abstract-content {
    margin-top: 8px;
    font-size: 0.95em;
    line-height: 1.5;
    color: inherit; /* 确保在黑底模式下也是亮的 */
    text-align: justify;
    opacity: 0.85; /* 稍微降点亮度增加高级感 */
  }

  /* 4. 控制列表项间距，减少空行 */
  .pub-item {
    margin-bottom: 1.2em !important; /* 压缩每一项之间的距离 */
  }
</style>

## Journal Articles / 期刊论文

{% for post in site.publications reversed %}
  {% if post.category == "manuscripts" %}
    <div class="pub-item">
      <h3 style="margin-bottom: 0.3em;"><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a></h3>
      <div style="font-size: 0.95em; margin-bottom: 0.4em;">{{ post.citation }}</div>
      <details>
        <summary>Abstract / 摘要 (点击展开)</summary>
        <div class="abstract-content">{{ post.content | strip_html }}</div>
      </details>
    </div>
  {% endif %}
{% endfor %}

## Working Papers / 工作论文

{% for post in site.publications reversed %}
  {% if post.category == "working_papers" %}
    <div class="pub-item">
      <h3 style="margin-bottom: 0.3em;"><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a></h3>
      {% if post.paperurl %}
        <div style="font-size: 0.9em;"><a href="{{ post.paperurl }}">[PDF Download]</a></div>
      {% endif %}
      <details>
        <summary>Abstract / 摘要 (点击展开)</summary>
        <div class="abstract-content">{{ post.content | strip_html }}</div>
      </details>
    </div>
  {% endif %}
{% endfor %}
