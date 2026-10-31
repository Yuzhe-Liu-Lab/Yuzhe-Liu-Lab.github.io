---
# Display name
title: Caizhi Ma(马才志)

# Full name (for SEO)
first_name: Caizhi
last_name: Ma

# Is this the primary user of the site?
superuser: false

# Role/position
role: PhD student, Class of 2025
entry_year: 2025

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
    马才志为2025级博士研究生，联合培养单位为北京航空航天大学-康复大学。其研究方向聚焦于基于血管神经耦合机制的运动和感觉功能障碍康复，以及脊髓损伤相关模型与太赫兹超材料传感技术。
  </p>

  <h3>联合培养导师</h3>
  <p>康复大学 王方永教授；北京航空航天大学 刘雨喆教授</p>

  <h3>教育经历</h3>

  <div>
    <p><i class="fas fa-graduation-cap"></i> 博士，生物医学工程，2025至今<br>
    <span style="color:gray;">北京航空航天大学</span></p>
  </div>
</div>

<div id="en" class="tabcontent" style="display:block;">
  <p>
    Caizhi Ma is a Ph.D. candidate in the Class of 2025 and is jointly trained by Beihang University and the University of Health and Rehabilitation Sciences. His research focuses on rehabilitation of motor and sensory dysfunction based on neurovascular coupling mechanisms, as well as spinal cord injury models and terahertz metamaterial sensing technologies.
  </p>

  <h3>Joint Training Supervisors</h3>
  <p>Prof. Fangyong Wang, University of Health and Rehabilitation Sciences; Prof. Yuzhe Liu, Beihang University</p>

  <h3>Education</h3>

  <div>
    <p><i class="fas fa-graduation-cap"></i> Ph.D. in Biomedical Engineering, 2025-Present<br>
    <span style="color:gray;">Beihang University</span></p>
  </div>
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
