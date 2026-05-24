---
# Display name
title: Xiaoyv Du(杜箫宇)

# Full name (for SEO)
first_name: Xiaoyv
last_name: Du

# Is this the primary user of the site?
superuser: false

# Role/position
role: Class of 2023
entry_year: 2023

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
#     link: 'mailto:test@example.org'
#   - icon: twitter
#     icon_pack: fab
#     link: https://twitter.com/GeorgeCushen
#   - icon: google-scholar
#     icon_pack: ai
#     link: https://scholar.google.co.uk/citations?user=sIwtMXoAAAAJ
#   - icon: github
#     icon_pack: fab
#     link: https://github.com/gcushen
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
  <button class="tablink" onclick="openTab('cn')">CN</button>
  <button class="tablink" onclick="openTab('en')">EN</button>
</div>


<!-- 中文版本 -->
<div id="cn" class="tabcontent" style="display:block;">

  <p>
    吳恩達是斯坦福大学人工智能实验室的教授。他的研究兴趣包括分布式机器人、移动计算和可编程物质。
    他领导的机器人神经生物学团队开发自重构机器人、自组织系统和移动传感网络。
  </p>

  <h3>兴趣</h3>
  <ul>
    <li>计算机科学</li>
    <li>运动</li>
  </ul>

  <h3>教育经历</h3>

<div>
  <p><i class="fas fa-graduation-cap"></i> 学士，生物医学工程，2023至今<br>
  <span style="color:gray;">北京航空航天大学</span></p>
</div>


</div>


<!-- 英文版本 -->
<div id="en" class="tabcontent" style="display:none;">
  <p>
    My major is Biomedical Engineering. Although I'm relatively new to coding, I have a strong interest in modeling, simulation, and computer-based approaches to understand real-world phenomena. In my spare time, I enjoy playing volleyball, rugby, swimming, and table tennis.
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


