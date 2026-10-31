---
# Display name
title: Xiaoyu Du(杜箫宇)

# Full name (for SEO)
first_name: Xiaoyu
last_name: Du

# Is this the primary user of the site?
superuser: false

# Role/position
role: PhD student, Class of 2027
entry_year: 2027

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
    杜箫宇，将作为2027级博士生在课题组继续研究，现主修生物医学工程。虽然接触编程的时间较短，但对建模、仿真以及利用计算机方法理解现实世界现象有浓厚兴趣。课余喜欢排球、橄榄球、游泳和乒乓球。
  </p>

  <h3>兴趣</h3>
  <ul>
    <li>计算科学</li>
    <li>运动</li>
  </ul>

  <h3>教育经历</h3>

<div>
  <p><i class="fas fa-graduation-cap"></i> 学士，生物医学工程，2023至今<br>
  <span style="color:gray;">北京航空航天大学</span></p>
</div>


</div>


<!-- 英文版本 -->
<div id="en" class="tabcontent" style="display:block;">
  <p>
    Xiaoyu Du will continue his research in the lab as a PhD student in the Class of 2027 and is currently majoring in Biomedical Engineering. Although relatively new to coding, he has a strong interest in modeling, simulation, and computer-based approaches to understanding real-world phenomena. In his spare time, he enjoys playing volleyball, rugby, swimming, and table tennis.
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


