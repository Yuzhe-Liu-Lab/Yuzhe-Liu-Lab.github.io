---
# Display name
title: Jiaming Liang(梁佳铭)

# Full name (for SEO)
first_name: Jiaming
last_name: Liang

# Is this the primary user of the site?
superuser: false

# Role/position
role: Class of 2024
entry_year: 2024

# Organizations/Affiliations
organizations:
  - name: Beihang University
    url: ''

# Enter email to display Gravatar (if Gravatar enabled in Config)
email: ''

# Organizational groups that you belong to (for People widget)
user_groups:
  - Undergraduate Students | 本科生
---

<style>
.tabs {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  border-right: 1px solid #ccc;
  width: 100%;
}

.tablink {
  border: 3px solid #ccc;
  border-left: none;
  border-top: none;
  padding: 4px 1px;
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

<div id="cn" class="tabcontent" style="display:none;">
  <p>
    梁佳铭是一名现读于北京航空航天大学生物与医学工程学院的学生，目前主要从事头部多刚体建模分析。热衷于对模型中的数学基础进行分析。
  </p>

  <h3>兴趣</h3>
  <ul>
    <li>应用数学</li>
    <li>计算机网络</li>
    <li>游泳</li>
  </ul>

  <h3>教育经历</h3>

  <div>
    <p><i class="fas fa-graduation-cap"></i> 学士，生物医学工程，2024至今<br>
    <span style="color:gray;">北京航空航天大学</span></p>
  </div>

  <h3>联系方式</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:liangjiaming@buaa.edu.cn">liangjiaming@buaa.edu.cn</a>
  </p>
</div>

<div id="en" class="tabcontent" style="display:block;">
  <p>
    Jiaming Liang is an undergraduate student at the School of Biomedical Engineering, Beihang University. He is currently engaged in multi-rigid body modeling and analysis of the head, and keen on exploring the mathematical fundamentals of relevant models.
  </p>

  <h3>Interests</h3>
  <ul>
    <li>Applied Mathematics</li>
    <li>Computer Networks</li>
    <li>Swimming</li>
  </ul>

  <h3>Education</h3>

  <div>
    <p><i class="fas fa-graduation-cap"></i> BSc in Biomedical Engineering, 2024-Present<br>
    <span style="color:gray;">Beihang University</span></p>
  </div>

  <h3>Contact</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:liangjiaming@buaa.edu.cn">liangjiaming@buaa.edu.cn</a>
  </p>
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
