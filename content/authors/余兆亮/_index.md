---
# Display name
title: Zhaoliang Yu(余兆亮)

# Full name (for SEO)
first_name: Zhaoliang
last_name: Yu

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
    余兆亮为博士研究生，其研究方向聚焦于脑机接口与脑科学，以及意识障碍的临床预测与评估。
  </p>

  <h3>教育经历</h3>

  <div>
    <p><i class="fas fa-graduation-cap"></i> 学士，电子科学与技术，2019至2023<br>
    <span style="color:gray;">北京邮电大学</span></p>
    <p><i class="fas fa-graduation-cap"></i> 硕士，生物医学工程，2023至2026<br>
    <span style="color:gray;">北京邮电大学</span></p>
    <p><i class="fas fa-graduation-cap"></i> 博士，生物医学工程，2026至今<br>
    <span style="color:gray;">北京航空航天大学</span></p>
  </div>

  <h3>联系方式</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:yuzhaoliangyzl@163.com">yuzhaoliangyzl@163.com</a>
  </p>
</div>

<div id="en" class="tabcontent" style="display:block;">
  <p>
    Zhaoliang Yu is a Ph.D. candidate. His research focuses on brain-computer interfaces and brain science, as well as the clinical prediction and assessment of disorders of consciousness.
  </p>

  <h3>Education</h3>

  <div>
    <p><i class="fas fa-graduation-cap"></i> BSc in Electronic Science and Technology, 2019-2023<br>
    <span style="color:gray;">Beijing University of Posts and Telecommunications</span></p>
    <p><i class="fas fa-graduation-cap"></i> MSc in Biomedical Engineering, 2023-2026<br>
    <span style="color:gray;">Beijing University of Posts and Telecommunications</span></p>
    <p><i class="fas fa-graduation-cap"></i> Ph.D. in Biomedical Engineering, 2026-Present<br>
    <span style="color:gray;">Beihang University</span></p>
  </div>

  <h3>Contact</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:yuzhaoliangyzl@163.com">yuzhaoliangyzl@163.com</a>
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
