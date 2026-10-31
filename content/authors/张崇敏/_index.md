---
# Display name
title: Chongmin Zhang(张崇敏)

# Full name (for SEO)
first_name: Chongmin
last_name: Zhang

# Is this the primary user of the site?
superuser: false

# Role/position
role: M.S. student, Class of 2025
entry_year: 2025

# Organizations/Affiliations
organizations:
  - name: Beihang University
    url: ''

# Short bio (displayed in user profile at end of posts)
# bio: My research interests include distributed robotics, mobile computing and programmable matter.

# interests:
#   - Artificial Intelligence
#   - Computational Linguistics
#   - Information Retrieval

# education:
#   courses:
#     - course: PhD in Artificial Intelligence
#       institution: Stanford University
#       year: 2012
#     - course: MEng in Artificial Intelligence
#       institution: Massachusetts Institute of Technology
#       year: 2009
#     - course: BSc in Artificial Intelligence
#       institution: Massachusetts Institute of Technology
#       year: 2008

# Social/Academic Networking
# For available icons, see: https://docs.hugoblox.com/getting-started/page-builder/#icons
#   For an email link, use "fas" icon pack, "envelope" icon, and a link in the
#   form "mailto:your-email@example.com" or "#contact" for contact widget.
# social:
#   - icon: envelope
#     icon_pack: fas
#     link: 'ljxxx@buaa.edu.cn'
#   - icon: github
#     icon_pack: fab
#     link: https://github.com/Thethumbtack
# Link to a PDF of your resume/CV from the About widget.
# To enable, copy your resume/CV to `static/files/cv.pdf` and uncomment the lines below.
# - icon: cv
#   icon_pack: ai
#   link: files/cv.pdf

# Enter email to display Gravatar (if Gravatar enabled in Config)
email: ''

# Organizational groups that you belong to (for People widget)
#   Set this to `[]` or comment out if you are not using People widget.
user_groups:
  - Master Students | 硕士生
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


<!-- 中文版本 -->
<div id="cn" class="tabcontent" style="display:none;">

  <p>
    张崇敏，2025级硕士研究生。主要研究方向为冲击中的头部运动学参数评估和深度学习在创伤性脑损伤评估中的应用。
  </p>

  <h3>兴趣</h3>
  <ul>
    <li>创伤性脑损伤</li>
    <li>人工智能</li>
  </ul>

  <h3>教育经历</h3>

<div>
  <p><i class="fas fa-graduation-cap"></i> 学士，生物医学工程，2021至2025<br>
  <span style="color:gray;">北京航空航天大学</span></p>
  <p><i class="fas fa-graduation-cap"></i> 硕士，生物医学工程，2025至今<br>
  <span style="color:gray;">北京航空航天大学</span></p>
</div>

  <h3>联系方式</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:zhangyihan@buaa.edu.cn">zhangyihan@buaa.edu.cn</a>
  </p>

</div>


<!-- 英文版本 -->
<div id="en" class="tabcontent" style="display:block;">
  <p>
    Chongmin Zhang is currently a master degree candidate. Her research focues on the evaluation of head kinematics during impact and the application of deea learning in traumatic brain injury assessment.
  </p>

  <h3>Interests</h3>
  <ul>
    <li>Traumatic Brain Injury</li>
    <li>Artificial Intelligence</li>
  </ul>

  <h3>Education</h3>

<div>
  <p><i class="fas fa-graduation-cap"></i> BSc in Biomedical Engineering, 2021-2025<br>
  <span style="color:gray;">Beihang University</span></p>
  <p><i class="fas fa-graduation-cap"></i> MSc in Biomedical Engineering, 2025-Present<br>
  <span style="color:gray;">Beihang University</span></p>
</div>

  <h3>Contact</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:cmin_zhang@163.com">cmin_zhang@163.com</a>
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


