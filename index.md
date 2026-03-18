<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <title>核物理会议信息</title>
  <style>
    table { border-collapse: collapse; width: 100%; }
    th, td { border: 1px solid #ccc; padding: 8px; text-align: center; }
    th { background-color: #f2f2f2; }
  </style>
</head>
<body>
  <h1>核物理会议列表</h1>
  <a href="submit.html">👉 提交会议</a>
  
  <table id="conferenceTable">
    <tr>
      <th>会议名称</th>
      <th>地点</th>
      <th>时间</th>
      <th>官网</th>
    </tr>
  </table>

  <script>
    // 这里可以把 _data/conferences.yml 转成 JSON 保存为 conferences.json
    const conferences = [
      {
        title: "全国核物理大会",
        location: "北京",
        start_date: "2026-05-12",
        end_date: "2026-05-16",
        link: "https://example.com"
      },
      {
        title: "核结构研讨会",
        location: "上海",
        start_date: "2026-06-20",
        end_date: "2026-06-23",
        link: "https://example.com"
      }
    ];

    const table = document.getElementById("conferenceTable");

    conferences.forEach(conf => {
      const row = document.createElement("tr");
      row.innerHTML = `
        <td>${conf.title}</td>
        <td>${conf.location}</td>
        <td>${conf.start_date} - ${conf.end_date}</td>
        <td><a href="${conf.link}" target="_blank">官网</a></td>
      `;
      table.appendChild(row);
    });
  </script>
</body>
</html>
