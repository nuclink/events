---
layout: default
title: 提交会议
---

# 📩 提交核物理会议

欢迎提交国内外核物理相关会议，我们会在审核后发布。

<form id="conferenceForm">
  会议名称:<br>
  <input type="text" name="title" required style="width:100%;"><br><br>

  地点:<br>
  <input type="text" name="location" required style="width:100%;"><br><br>

  开始日期:<br>
  <input type="date" name="start_date" required><br><br>

  结束日期:<br>
  <input type="date" name="end_date" required><br><br>

  投稿截止日期:<br>
  <input type="date" name="deadline"><br><br>

  官方网站:<br>
  <input type="url" name="link" required style="width:100%;"><br><br>

  备注（可选）:<br>
  <textarea name="note" style="width:100%; height:100px;"></textarea><br><br>

  <button type="submit" style="padding:10px 20px;">提交会议</button>
</form>

<div id="message" style="margin-top:15px;color:green;"></div>

<script>
document.getElementById("conferenceForm").addEventListener("submit", async function(e){
  e.preventDefault();
  // 获取表单数据
  const data = {
    title: this.title.value,
    location: this.location.value,
    start_date: this.start_date.value,
    end_date: this.end_date.value,
    deadline: this.deadline.value,
    link: this.link.value,
    note: this.note.value
  };
  
  // 这里我们先做“测试”，提交到浏览器控制台
  console.log("提交数据:", data);
  
  document.getElementById("message").innerText = "数据已提交，等待审核上线！";
  this.reset();
});
</script>
