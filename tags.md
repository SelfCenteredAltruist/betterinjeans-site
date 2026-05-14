---
layout: default
title: Tags
---

<h1 class="page-title">Tags</h1>

<ul class="tag-list">
  {% assign tags = site.tags | sort %}
  {% for tag in tags %}
    <li>
      <a class="tag-link" href="{{ '/tag/' | append: tag[0] | relative_url }}">
        {{ tag[0] }}
      </a>
      <span class="tag-count">{{ tag[1].size }}</span>
    </li>
  {% endfor %}
</ul>

<h2 class="tag-cloud-title">Tag Cloud</h2>

<div class="tag-cloud">
  {% assign tags = site.tags %}
  {% for tag in tags %}
    {% assign count = tag[1].size %}
    {% assign size = count | times: 4 | plus: 12 %}
    <a 
      href="{{ '/tag/' | append: tag[0] | relative_url }}" 
      style="font-size: {{ size }}px;"
      class="tag-cloud-item"
    >
      {{ tag[0] }}
    </a>
  {% endfor %}
</div>
