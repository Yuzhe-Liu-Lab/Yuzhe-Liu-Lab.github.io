---
# Display name
title: Junxi Liu(刘俊希)

# Full name (for SEO)
first_name: Junxi
last_name: Liu

# Is this the primary user of the site?
superuser: false

# Role/position
role: Class of 2024

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
social:
  # - icon: envelope
  #   icon_pack: fas
  #   link: 'ljxxx@buaa.edu.cn'
  - icon: github
    icon_pack: fab
    link: https://github.com/Thethumbtack
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
  - Undergraduate Students | 本科生
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
    刘俊希是北京航空航天大学生物医学工程专业的在读本科生。他目前的研究方向是应用机器学习方法，提升脑损伤诊断的准确性与速度，致力于实现碰撞等创伤事件后的快速诊断与评估。<br>
    除核心研究外，俊希也积极探索3D打印、嵌入式系统开发等不同技术领域。他热衷于融合跨学科知识，以创造富有创新性的解决方案。
  </p>

  <h3>兴趣</h3>
  <ul>
    <li>大语言模型 (LLM)</li>
    <li>机器学习</li>
    <li>数据科学</li>
  </ul>

  <h3>教育经历</h3>

<div>
  <p><i class="fas fa-graduation-cap"></i> 学士，生物医学工程，2024至今<br>
  <span style="color:gray;">北京航空航天大学</span></p>
</div>

<h3>联系方式</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:ljxxx@buaa.edu.cn">ljxxx@buaa.edu.cn</a>
  </p>

</div>


<!-- 英文版本 -->
<div id="en" class="tabcontent" style="display:block;">
  <p>
    Junxi Liu is an undergraduate student majoring in Biomedical Engineering at Beihang University. His current research focuses on applying machine learning techniques to enhance the accuracy and speed of brain injury diagnosis, with a particular emphasis on enabling rapid assessment after traumatic impacts such as collisions.<br><br>
    Beyond his primary research, Junxi is also actively exploring various interdisciplinary fields, including 3D printing and embedded systems development. He is passionate about leveraging diverse technologies to create innovative solutions.
  </p>

  <h3>Interests</h3>
  <ul>
    <li>Computational Science</li>
    <li>Sports</li>
  </ul>

  <h3>Education</h3>

<div>
  <p><i class="fas fa-graduation-cap"></i> BSc in Biomedical Engineering, 2023-Present<br>
  <span style="color:gray;">Beihang University</span></p>
</div>

<h3>Contact</h3>
  <p>
    <i class="fas fa-envelope"></i> <a href="mailto:ljxxx@buaa.edu.cn">ljxxx@buaa.edu.cn</a>
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


