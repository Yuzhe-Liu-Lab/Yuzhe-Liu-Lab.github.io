---
# Display name
title: Yonglin Chen(陈永霖)

# Full name (for SEO)
first_name: Yonglin
last_name: Chen

# Is this the primary user of the site?
superuser: false

# Role/position
role: B.S. Graduate, Class of 2023
entry_year: 2023

# Organizations/Affiliations
organizations:
  - name: Tsinghua University
    url: ''

# Enter email to display Gravatar (if Gravatar enabled in Config)
email: ''

# Organizational groups that you belong to (for People widget)
user_groups:
  - Alumni | 毕业生
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
    陈永霖曾于2023年作为本科生在本课题组开展科研工作，现为清华大学生物医学工程专业硕士研究生。他的研究方向包括减震器动态力学特性、医学影像后处理算法开发，以及磁共振脉冲序列的优化设计。
  </p>

  <h3>兴趣</h3>
  <ul>
    <li>创伤性脑损伤</li>
    <li>人工智能</li>
  </ul>

  <h3>教育经历</h3>

  <div>
    <p><i class="fas fa-graduation-cap"></i> 学士，生物医学工程，2020至2024<br>
    <span style="color:gray;">北京航空航天大学</span></p>
    <p><i class="fas fa-graduation-cap"></i> 硕士，生物医学工程，2024至今<br>
    <span style="color:gray;">清华大学</span></p>
  </div>

  <h3>联系方式</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:ylchen9331@163.com">ylchen9331@163.com</a>
  </p>
</div>

<div id="en" class="tabcontent" style="display:block;">
  <p>
    Yonglin Chen conducted undergraduate research in the lab in 2023 and is currently a master's student in Biomedical Engineering at Tsinghua University. His research focuses on the dynamic mechanical characterization of shock absorbers, the development of medical image post-processing algorithms, and the optimization of MRI pulse sequences.
  </p>

  <h3>Interests</h3>
  <ul>
    <li>Traumatic Brain Injury</li>
    <li>Artificial Intelligence</li>
  </ul>

  <h3>Education</h3>

  <div>
    <p><i class="fas fa-graduation-cap"></i> BSc in Biomedical Engineering, 2020-2024<br>
    <span style="color:gray;">Beihang University</span></p>
    <p><i class="fas fa-graduation-cap"></i> MSc in Biomedical Engineering, 2024-Present<br>
    <span style="color:gray;">Tsinghua University</span></p>
  </div>

  <h3>Contact</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:ylchen9331@163.com">ylchen9331@163.com</a>
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
