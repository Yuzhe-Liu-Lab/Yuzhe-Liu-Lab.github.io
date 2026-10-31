---
# Display name
title: Panyu Jiang(姜泮宇)

# Full name (for SEO)
first_name: Panyu
last_name: Jiang

# Is this the primary user of the site?
superuser: false

# Role/position
role: PhD student, Class of 2026
entry_year: 2026

# Organizations/Affiliations
organizations:
  - name: Beihang University
    url: ''

# Enter email to display Gravatar (if Gravatar enabled in Config)
email: ''

# Organizational groups that you belong to (for People widget)
user_groups:
  - PhD Students | 博士生
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
    姜泮宇，2026级博士研究生。研究方向主要为超声响应压电生物材料及其在多种疾病模型中的应用。
  </p>

  <h3>合作指导导师</h3>
  <p>北京航空航天大学 曹芳芳教授</p>

  <h3>教育经历</h3>

  <div>
    <p><i class="fas fa-graduation-cap"></i> 学士，生物医学工程，2019至2023<br>
    <span style="color:gray;">华南理工大学</span></p>
    <p><i class="fas fa-graduation-cap"></i> 硕士，生物医学工程，2023至2026<br>
    <span style="color:gray;">河北工业大学</span></p>
    <p><i class="fas fa-graduation-cap"></i> 博士，生物医学工程，2026至今<br>
    <span style="color:gray;">北京航空航天大学</span></p>
  </div>

  <h3>联系方式</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:jiangpanyu0904@163.com">jiangpanyu0904@163.com</a>
  </p>
</div>

<div id="en" class="tabcontent" style="display:block;">
  <p>
    Panyu Jiang is a Ph.D. candidate. His research focuses on ultrasonic-responsive piezoelectric biological materials and their applications in various disease models.
  </p>

  <h3>Co-Supervisor</h3>
  <p>Prof. Fangfang Cao, Beihang University</p>

  <h3>Education</h3>

  <div>
    <p><i class="fas fa-graduation-cap"></i> BSc in Biomedical Engineering, 2019-2023<br>
    <span style="color:gray;">South China University of Technology</span></p>
    <p><i class="fas fa-graduation-cap"></i> MSc in Biomedical Engineering, 2023-2026<br>
    <span style="color:gray;">Hebei University of Technology</span></p>
    <p><i class="fas fa-graduation-cap"></i> Ph.D. in Biomedical Engineering, 2026-Present<br>
    <span style="color:gray;">Beihang University</span></p>
  </div>

  <h3>Contact</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:jiangpanyu0904@163.com">jiangpanyu0904@163.com</a>
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
