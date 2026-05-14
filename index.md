---
layout: default
title: Home
---

<div class="hero">
  <h1 class="hero-title">Better in Jeans</h1>
  <p class="hero-subtitle">
    What finds its way back always finds me better in jeans - authentic inevitability
  </p>
</div>

---

# Latest Posts

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="post-date">{{ post.date | date: "%B %-d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>

