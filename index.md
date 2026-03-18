---
layout: default
title: 核物理会议信息
---

# 核物理会议列表

[👉 提交会议](submit)

<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th>会议名称</th>
    <th>地点</th>
    <th>时间</th>
    <th>投稿截止</th>
    <th>官网</th>
  </tr>
  {% for conf in site.data.conferences %}
  <tr>
    <td>{{ conf.title }}</td>
    <td>{{ conf.location }}</td>
    <td>{{ conf.start_date }} - {{ conf.end_date }}</td>
    <td>{{ conf.deadline }}</td>
    <td><a href="{{ conf.link }}">官网</a></td>
  </tr>
  {% endfor %}
</table>
