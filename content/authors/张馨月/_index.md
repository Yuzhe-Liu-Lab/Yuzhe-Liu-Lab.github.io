---
title: Xinyue Zhang(张馨月)
first_name: Xinyue
last_name: Zhang
superuser: false
role: PhD student, Class of 2027
entry_year: 2027
organizations:
  - name: Beihang University
    url: ''
email: ''
user_groups:
  - PhD Students | 博士生
---

<style>
.tabs {
  display: flex;
  flex-direction: row;       /* 横向排列 */
  justify-content: flex-end; /* 按钮靠右 */
  border-right: 1px solid #ccc; /* 浅灰色右边框 */
  width: 100%;
}

.tablink {
  border: 3px solid #ccc; /* 浅灰色边框 */
  border-left: none;
  border-top: none;
  padding:  4px 1px;
  cursor: pointer;
  width: 50px;
  font-size: 13px;
  text-align: center;
  background-color: white;
  font-family: "Arial Rounded MT Bold", sans-serif;
  border-radius: 8px;
}
</style>

<div class="tabs">
  <button class="tablink" onclick="openTab('en')">EN</button>
  <button class="tablink" onclick="openTab('cn')">CN</button>
</div>

<div id="en" class="tabcontent" style="display:block;">
<p>Xinyue Zhang graduated from Beihang University with a bachelor's degree in 2026 and will join the lab as a PhD student in the Class of 2027.</p>
<h3>Interests</h3>
<ul>
  <li>Computational Neuroscience</li>
  <li>Connectomics</li>
  <li>Neural Circuit Research in Small-Animal Models</li>
</ul>
<h3>Education</h3>
<p><i class="fas fa-graduation-cap"></i> Bachelor's degree, graduated in 2026<br><span style="color:gray;">Beihang University</span></p>
</div>

<div id="cn" class="tabcontent" style="display:none;">
<p>张馨月，北京航空航天大学2026届本科毕业生，将作为2027级博士生加入课题组。</p>
<h3>兴趣</h3>
<ul>
  <li>计算神经科学</li>
  <li>连接组学</li>
  <li>小动物模型神经环路研究</li>
</ul>
<h3>教育经历</h3>
<p><i class="fas fa-graduation-cap"></i> 学士，2026届毕业<br><span style="color:gray;">北京航空航天大学</span></p>
</div>

<script>
function openTab(tabName) {
  var i, x;
  x = document.getElementsByClassName("tabcontent");
  for (i = 0; i < x.length; i++) {
    x[i].style.display = "none";
  }
  document.getElementById(tabName).style.display = "block";
}
</script>
