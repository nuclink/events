---
layout: default
title: 核物理会议信息
---

# 核物理会议列表

<ul>
{% for conf in site.data.conferences %}
  <li>
    <strong>{{ conf.title }}</strong><br>
    地点：{{ conf.location }}<br>
    时间：{{ conf.start_date }} - {{ conf.end_date }}
    <a href="{{ conf.link }}">官网</a>
  </li>
{% endfor %}
</ul>
