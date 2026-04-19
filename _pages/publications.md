---
layout: archive
title: "Publications / 论文"
permalink: /publications/
author_profile: true
---

<style>
  /* 彻底消除顶部留白 */
  .page__header, .page__title { display: none !important; }
  .archive { margin-top: 0 !important; }
  #main { padding-top: 1em !important; }
  
  /* 调整标题间距，解决“过宽”问题 */
  h2 {
    margin-top: 1.5em !important; /* 调整两个板块之间的距离 */
    margin-bottom: 0.5em !important;
  }
  hr { margin-top: 0.2em !important; }
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
    <div class="list__item">
      <article class="archive__item">
        <h2 class="archive__item-title">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </h2>
        <p class="archive__item-excerpt">
          {% if post.citation %}
            {{ post.citation }}
          {% else %}
            {{ post.title }}. <i>Working Paper</i>, {{ post.date | date: '%Y' }}.
          {% endif %}
          {% if post.paperurl %}
            <br /><a href="{{ post.paperurl }}">Download Paper</a>
          {% endif %}
        </p>
      </article>
    </div>
  {% endif %}
{% endfor %}
