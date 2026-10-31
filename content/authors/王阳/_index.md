---
# Display name
title: Yang Wang(王阳)

# Full name (for SEO)
first_name: Yang
last_name: Wang

# Is this the primary user of the site?
superuser: false

# Role/position
role: PhD student, Class of 2024
entry_year: 2024

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


<!-- 中文版本 -->
<div id="cn" class="tabcontent" style="display:none;">

  <p>
    王阳，2024级博士研究生。研究方向主要为中低应变率下多稳态超材料结构设计及头部冲击防护应用。
  </p>

  <!-- <h3>兴趣</h3>
  <ul>
    <li>阅读</li>
    <li>摄影</li>
    <li>游泳</li>
  </ul> -->

  <h3>教育经历</h3>

<div>
  <p><i class="fas fa-graduation-cap"></i> 学士，机械设计制造及其自动化，2016至2020<br>
  <span style="color:gray;">河南科技大学</span></p>
  <p><i class="fas fa-graduation-cap"></i> 硕士，机械工程，2021至2024<br>
  <span style="color:gray;">太原理工大学</span></p>
  <p><i class="fas fa-graduation-cap"></i> 博士，生物医学工程，2024至今<br>
  <span style="color:gray;">北京航空航天大学</span></p>
</div>

  <h3>联系方式</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:by2410213@buaa.edu.cn">by2410213@buaa.edu.cn</a>
  </p>

</div>


<!-- 英文版本 -->
<div id="en" class="tabcontent" style="display:block;">
  <p>
    Yang Wang is a Ph.D. candidate. His research focuses on design and performance analysis of multi-stable metamaterials under low-to-moderate strain rates for head impact protection.
  </p>

  <!-- <h3>Interests</h3>
  <ul>
    <li>Reading</li>
    <li>Photography</li>
    <li>Swimming</li>
  </ul> -->

  <h3>Education</h3>

<div>
  <p><i class="fas fa-graduation-cap"></i> BSc in Mechanical Engineering and Automation, 2016-2020<br>
  <span style="color:gray;">Henan University of Science and Technology</span></p>
  <p><i class="fas fa-graduation-cap"></i> MSc in Mechanical Engineering, 2021-2024<br>
  <span style="color:gray;">Taiyuan University of Technology</span></p>
  <p><i class="fas fa-graduation-cap"></i> Ph.D. in Biomedical Engineering, 2024-Present<br>
  <span style="color:gray;">Beihang University</span></p>
</div>

  <h3>Contact</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:by2410213@buaa.edu.cn">by2410213@buaa.edu.cn</a>
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


