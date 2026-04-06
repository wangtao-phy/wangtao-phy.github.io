---
layout: page
title: Jottings
permalink: /jottings/
---

## 我的随笔

<ul>
  {% for jot in site.jottings %}
    <li>
      <a href="{{ jot.url }}">{{ jot.title }}</a>
      <span style="font-size: 0.8rem; color: #888;"> - {{ jot.date | date: "%Y年%m月%d日" }}</span>
    </li>
  {% endfor %}
</ul>
