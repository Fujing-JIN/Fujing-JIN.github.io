---
layout: single
title: ""
permalink: /publications/
author_profile: true
---

<style>
  /* 1. 彻底移除顶部空白 */
  .page__header, .page__title, .breadcrumbs { display: none !important; }
  #main { padding-top: 0 !important; margin-top: 0 !important; }
  .page__inner-wrap { padding-top: 0 !important; margin-top: 0 !important; }

  /* 2. 控制板块间距：让“工作论文”标题不那么靠下 */
  h2 { margin-top: 1.2em !important; margin-bottom: 0.5em !important; }
  .archive__item { margin-bottom: 1.5em !important; }
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
### [{{ post.title }}]({{ base_path }}{{ post.url }})
{{ post.citation }} {% if post.paperurl %}[[PDF]({{ post.paperurl }})]{% endif %}
  {% endif %}
{% endfor %}
