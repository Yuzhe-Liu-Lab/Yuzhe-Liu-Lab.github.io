---
# Display name
title: Luoming Xu(许洛铭)

# Full name (for SEO)
first_name: Luoming
last_name: Xu

# Is this the primary user of the site?
superuser: false

# Role/position
role: M. S. student, Class of 2026
entry_year: 2026

# Organizations/Affiliations
organizations:
  - name: Beihang University
    url: ''

# Enter email to display Gravatar (if Gravatar enabled in Config)
email: ''

# Organizational groups that you belong to (for People widget)
user_groups:
  - Master Students | 硕士生
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
    许洛铭，2026级硕士研究生，主要研究方向为头部冲击条件下的运动学参数评估、脑外伤模型的构建与预测。
  </p>

  <h3>兴趣</h3>
  <ul>
    <li>创伤性脑损伤</li>
    <li>生物力学</li>
  </ul>

  <h3>教育经历</h3>

  <div>
    <p><i class="fas fa-graduation-cap"></i> 学士，生物医学工程，2022至2026<br>
    <span style="color:gray;">首都医科大学</span></p>
    <p><i class="fas fa-graduation-cap"></i> 硕士，生物医学工程，2026至今<br>
    <span style="color:gray;">北京航空航天大学</span></p>
  </div>

  <h3>联系方式</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:luoming_xu04@163.com">luoming_xu04@163.com</a>
  </p>
</div>

<div id="en" class="tabcontent" style="display:block;">
  <p>
    Luoming Xu is currently a master's degree candidate. His research focuses on the evaluation of head kinematic parameters under impact conditions, as well as the construction and prediction of traumatic brain injury models.
  </p>

  <h3>Interests</h3>
  <ul>
    <li>Traumatic Brain Injury</li>
    <li>Biomechanics</li>
  </ul>

  <h3>Education</h3>

  <div>
    <p><i class="fas fa-graduation-cap"></i> BSc in Biomedical Engineering, 2022-2026<br>
    <span style="color:gray;">Capital Medical University</span></p>
    <p><i class="fas fa-graduation-cap"></i> MSc in Biomedical Engineering, 2026-Present<br>
    <span style="color:gray;">Beihang University</span></p>
  </div>

  <h3>Contact</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:luoming_xu04@163.com">luoming_xu04@163.com</a>
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
