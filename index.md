<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th>会议名称</th>
    <th>地点</th>
    <th>时间</th>
    <th>官网</th>
  </tr>
  {% for conf in site.data.conferences %}
  <tr>
    <td>{{ conf.title }}</td>
    <td>{{ conf.location }}</td>
    <td>{{ conf.start_date }} - {{ conf.end_date }}</td>
    <td><a href="{{ conf.link }}" target="_blank">官网</a></td>
  </tr>
  {% endfor %}
</table>
