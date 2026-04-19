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
    <div class="list__item">
      <article class="archive__item" itemscope itemtype="http://schema.org/CreativeWork">
        <h2 class="archive__item-title" itemprop="headline">
          {% if post.link %}
            <a href="{{ post.link }}">{{ post.title }}</a> <a href="{{ base_path }}{{ post.url }}" rel="permalink"><i class="fa fa-link" aria-hidden="true" title="permalink"></i><span class="sr-only">Permalink</span></a>
          {% else %}
            <a href="{{ base_path }}{{ post.url }}" rel="permalink">{{ post.title }}</a>
          {% endif %}
        </h2>
        
        <p class="archive__item-excerpt" itemprop="description">
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
