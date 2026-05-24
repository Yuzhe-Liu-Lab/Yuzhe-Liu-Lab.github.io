# Yuzhe Lab Website Update Guide

This document records the practical workflow for maintaining the Yuzhe Lab website. It is intended to be detailed enough that future updates can follow it directly without re-asking the same formatting and implementation questions.

The site is a Hugo / Hugo Blox research group website. The actual repository root is:

```text
D:\Works_ThinkpadT14p\LabWebsite\Sites_team\Yuzhe-Liu-Lab.github.io
```

Do not confuse it with the parent folder:

```text
D:\Works_ThinkpadT14p\LabWebsite\Sites_team
```

## Core Rules

1. Edit source files under `content`, `assets`, `config`, and occasionally `static`.
2. `public` is generated output. Only copy into `public` when a live local preview must be refreshed and Hugo is blocked by a stale process. Source files remain the authority.
3. Files are UTF-8. PowerShell may display Chinese as mojibake, but the files can still be correct. Verify Chinese with Python UTF-8 reads if needed.
4. Use English first, Chinese second for public-facing bilingual content, unless an existing local pattern says otherwise.
5. For lab members in publication authors, use the format:

```text
Yuzhe Liu(刘雨喆)
Yihan Zhang(张艺涵)
Yang Wang(王阳)
Xiaoyu Du(杜箫宇)
```

External collaborators should keep the name style used by the paper or official page.

## Useful Commands

Run these from the repository root.

Build:

```powershell
hugo --minify --noBuildLock
```

If default output or cache is blocked by a stale Hugo process, build to a temporary directory:

```powershell
hugo --logLevel info --noBuildLock --destination D:\Works_ThinkpadT14p\LabWebsite\Sites_team\Yuzhe-Liu-Lab.github.io\public-test
```

Local preview:

```powershell
hugo server --bind 127.0.0.1 --port 1313 --disableFastRender
```

Check stale Hugo processes:

```powershell
Get-CimInstance Win32_Process | Where-Object { $_.Name -like 'hugo*' } | Select-Object ProcessId,Name,CommandLine,CreationDate
```

Terminate stale Hugo processes that were started by the current update:

```powershell
taskkill /F /PID <PID>
```

Some old `hugo.exe` processes may be owned by another user/session and return `Access is denied`. If so, do not fight it endlessly. Use `--noBuildLock`, a temporary destination, or restart the terminal/app.

Search content:

```powershell
rg -n "search text" content
rg --files content\publication
```

Verify Chinese content without PowerShell encoding confusion:

```powershell
@'
from pathlib import Path
p = Path(r"D:\Works_ThinkpadT14p\LabWebsite\Sites_team\Yuzhe-Liu-Lab.github.io\content\post\example\index.md")
txt = p.read_text(encoding="utf-8")
print("本科生" in txt)
print(txt.splitlines()[1].encode("unicode_escape").decode("ascii"))
'@ | python -
```

## Homepage

Main file:

```text
content/_index.md
```

The current homepage slider background order is:

```yaml
slides:
  - background:
      image:
        filename: coders.jpg
  - background:
      image:
        filename: coder1.jpg
  - background:
      image:
        filename: coder2.jpg
```

Images are stored in:

```text
assets/media/coders.jpg
assets/media/coder1.jpg
assets/media/coder2.jpg
```

If the homepage turns gray, check:

1. The filenames in `content/_index.md`.
2. The files exist in `assets/media`.
3. Generated output has the files in `public/media`.
4. The CSS fallback exists in `assets/scss/custom.scss`:

```scss
#section-slider .carousel-item:nth-of-type(1) {
  background-image: url('/media/coders.jpg') !important;
}

#section-slider .carousel-item:nth-of-type(2) {
  background-image: url('/media/coder1.jpg') !important;
}

#section-slider .carousel-item:nth-of-type(3) {
  background-image: url('/media/coder2.jpg') !important;
}
```

This fallback avoids broken absolute preview URLs such as `http://localhost:1313/media/...`.

## Menus

Main menu file:

```text
config/_default/menus.yaml
```

Current order:

```yaml
main:
  - name: People
    url: people
    weight: 30
  - name: News
    url: post
    weight: 20
  - name: Publications
    url: publication
    weight: 50
  - name: Resources
    url: resources
    weight: 55
  - name: Contact
    url: contact
    weight: 60
```

If a menu button goes to Page Not Found, check the `url` here. Use section paths like `people`, `post`, `publication`, `resources`, `contact`.

## News Format

News posts live under:

```text
content/post/<date-slug>/index.md
```

Use English title first, then Chinese in parentheses. Body should also be English first, Chinese second. The News list page uses the first paragraph or `summary`, so add a bilingual `summary` when the list should show both languages.

Template:

```markdown
---
title: English News Title (中文新闻标题)
date: 2026-05-24
summary: |
  One short English summary sentence.
  一句简短中文摘要。
image:
  focal_point: 'center'
---

English paragraph 1.

English paragraph 2.

中文段落 1。

中文段落 2。
```

Example style:

```markdown
---
title: Undergraduate Xiaoyu Du Approved for the Beijing Natural Science Foundation Undergraduate Qiyan Program (本科生杜箫宇获批北京市自然科学基金本科生“启研”计划)
date: 2026-05-24
summary: |
  Undergraduate student Xiaoyu Du has been approved for the Beijing Natural Science Foundation Undergraduate Qiyan Program.
  本科生杜箫宇获批北京市自然科学基金本科生“启研”计划。
image:
  focal_point: 'center'
---

Undergraduate student Xiaoyu Du has been approved for the Beijing Natural Science Foundation Undergraduate Qiyan Program. The project is titled "Characterizing Cognitive Impairment in Traumatic Brain Injury Using Multimodal Imaging and Investigating Its Biomechanical Mechanisms."

This project focuses on the challenge of individualized characterization of cognitive impairment in mild traumatic brain injury...

本科生杜箫宇获批北京市自然科学基金本科生“启研”计划，课题题目为“基于多模态影像的创伤性脑损伤认知损伤表征及损伤生物力学机制研究”。

该课题聚焦轻度创伤性脑损伤中认知损伤难以个体化表征的问题...
```

News checks:

```powershell
hugo --minify --noBuildLock
```

Then check:

```text
public/post/index.html
public/post/<date-slug>/index.html
```

Confirm the list page title and summary are English first, Chinese second.

## People And Author Pages

Author pages live under:

```text
content/authors/<中文姓名>/_index.md
content/authors/<中文姓名>/avatar.jpg
```

The People page is:

```text
content/people/index.md
```

Current People groups:

```yaml
user_groups:
  - Principal Investigator | 课题组负责人
  - Researchers | 研究人员
  - PhD Students | 博士生
  - Master Students | 硕士生
  - Undergraduate Students | 本科生
  - Administration | 行政人员
  - Visitors | 访问学生
  - Alumni | 毕业生
sort_by: Params.entry_year
sort_ascending: true
```

For students, add:

```yaml
role: PhD student, Class of 2026
entry_year: 2026
user_groups:
  - PhD Students | 博士生
```

or:

```yaml
role: M.S. student, Class of 2025
entry_year: 2025
user_groups:
  - Master Students | 硕士生
```

or:

```yaml
role: Class of 2024
entry_year: 2024
user_groups:
  - Undergraduate Students | 本科生
```

Author page body should follow the existing tabbed EN/CN style. If adding a co-supervisor, include it in both languages:

```html
<h3>Co-Supervisor</h3>
<p>Prof. Fangfang Cao, Beihang University</p>
```

```html
<h3>合作指导导师</h3>
<p>北京航空航天大学 曹芳芳教授</p>
```

Avatar convention:

```text
avatar.jpg
```

Use `avatar.png` only if the existing page already does so.

## Publications

Publication pages live under:

```text
content/publication/<slug>/index.md
content/publication/<slug>/featured.jpg
```

PDF source folders used during the large update:

```text
D:\Works_ThinkpadT14p\LabWebsite\一作通讯论文
D:\Works_ThinkpadT14p\LabWebsite\其他论文
```

When asked to reconcile PDFs and website publications:

1. Count all PDFs in the folders.
2. Identify supplements and duplicates.
3. Check that every independent paper has a `content/publication/<slug>/index.md`.
4. If a PDF is not on the site, create a new publication entry.
5. Keep a short skip list for supplements/duplicates, with reason.

Publication front matter template:

```markdown
---
title: "Paper Title"
authors:
  - First Author
  - Lab Member(中文名)
  - Yuzhe Liu(刘雨喆)
date: "2026-05-22T00:00:00Z"
doi: "10.xxxx/xxxxx"
links:
  - name: Source Document
    url: "https://official.publisher.page/or/official/article/page"

publishDate: "2026-05-22T00:00:00Z"

publication_types: ["Journal"]

publication: "Full Journal Name"
publication_short: "Journal Abbrev."

abstract: ""
summary: ""

tags: ["tag one", "tag two"]
featured: false

image:
  filename: "featured.jpg"
  caption: "Short caption."
  focal_point: "Center"
  preview_only: true
---

![Short caption.](featured.jpg)

## Abstract

Abstract text...
```

Important publication rules:

1. `publication_types` must be exactly:

```yaml
publication_types: ["Journal"]
```

Do not use `"2"`.

2. Add DOI:

```yaml
doi: "10.1007/s10439-026-04174-x"
```

3. Add official page as Source Document:

```yaml
links:
  - name: Source Document
    url: "https://link.springer.com/10.1007/s10439-026-04174-x"
```

4. Verify DOI using official publisher pages, Crossref, PubMed, or the PDF first page. Do not guess.
5. In lab member names, use `English Name(中文名)`.
6. In outside collaborator names, keep the official spelling from the paper.
7. The body image should appear after the title/authors/buttons area and before Abstract. This is achieved by placing:

```markdown
![Caption](featured.jpg)

## Abstract
```

after the front matter.

8. Publication images should be wide/horizontal when possible, avoid plain curve plots, and prefer visually expressive figures, diagrams, model results, or representative screenshots from the PDF.

### Publication Image Workflow

Goal: use a wide image with minimal white margins.

1. Open/render PDF pages.
2. Search for figures that are wider than tall.
3. Avoid line charts unless no better option exists.
4. Prefer mechanism diagrams, model/brain strain fields, experimental setups, finite element visualizations, or representative workflows.
5. Crop the figure tightly. Avoid large white space above/below.
6. Save as:

```text
content/publication/<slug>/featured.jpg
```

7. Add front matter image metadata and body image markdown.
8. Build and visually check the publication page.

If processing images programmatically, the bundled Python usually has Pillow:

```powershell
@'
from PIL import Image
print("Pillow OK")
'@ | & 'C:\Users\Lenovo\.cache\codex-runtimes\codex-primary-runtime\dependencies\python\python.exe' -
```

For bulk crop/cleanup, use content bounding boxes where possible and keep the output JPEG/web image horizontal.

### Publication DOI And Source Document Checklist

For every paper:

1. DOI in front matter.
2. `Source Document` link points to official article page, not a random PDF mirror.
3. `publication_types: ["Journal"]`.
4. Authors checked.
5. Lab author names are unified.
6. Abstract exists.
7. `featured.jpg` exists and is not blank.
8. Body image appears before `## Abstract`.
9. Build passes.

## Resources

Resources main page:

```text
content/resources/_index.md
```

Resource subpages:

```text
content/resources/<slug>/index.md
content/resources/<slug>/featured.jpg   # optional, auto displayed as page header
```

Use `_index.md`, not `index.md`, for the Resources section root. If `content/resources/index.md` is used, Hugo may treat Resources as a leaf page and subpages may not generate.

Resources main page should be a simple overview: title plus one-sentence summary for each resource.

Current main-page structure:

```markdown
---
title: Resources | 开源资源
date: 2026-05-24
type: landing

sections:
  - block: markdown
    content:
      title: Resources
      text: |
        Resources from the Yuzhe Liu Lab include open-source computational tools and research devices for head-impact biomechanics.

        ## [Instrumented Mouthguard](instrumented-mouthguard/)

        A custom-fit smart mouthguard... 智能牙套...

        ## [Deep Learning Brain Model](deep-learning-brain-model/)

        A deep learning model... 深度学习大脑模型...

        ## [Brain-RBF](brain-rbf/)

        A radial-basis-function workflow...
---
```

Resource subpage format:

```markdown
---
title: Resource Name | 中文名
date: 2026-05-24
---

## Introduction

English introduction.

If you are interested in using the resource or collaborating with us, please contact us.

## 中文介绍

中文介绍。

如需使用该资源或开展合作，请联系我们。

## Related Publications

- [Paper Title](/publication/paper-slug/)
```

If a resource has `featured.jpg`, Hugo automatically displays it at the top of the page. Do not also add:

```markdown
![Resource image](featured.jpg)
```

unless the design intentionally needs a second inline copy. This caused duplicate images on `Instrumented Mouthguard`.

### Current Resources

#### Instrumented Mouthguard | 智能牙套

Path:

```text
content/resources/instrumented-mouthguard/index.md
content/resources/instrumented-mouthguard/featured.jpg
```

Content requirements:

1. English first, Chinese second.
2. Describe customized assembly interface.
3. Describe six-axis head kinematics measurement.
4. Mention high-bandwidth inertial sensors.
5. Mention Bluetooth wireless data transfer.
6. Mention wireless charging.
7. Include contact sentence only.
8. Include collaborator:

```text
Associate Professor Li Wang, Beihang University.
北京航空航天大学 王立副教授。
```

Related publications:

```markdown
- [Validation and Comparison of Instrumented Mouthguards for Measuring Head Kinematics and Assessing Brain Deformation in Football Impacts](/publication/2020-mg/)
- [Identifying Factors Associated with Head Impact Kinematics and Brain Strain in High School American Football via Instrumented Mouthguards](/publication/2021-highschool/)
- [Time Window of Head Impact Kinematics Measurement for Calculation of Brain Strain and Strain Rate in American Football](/publication/2022-timewindows/)
- [AI-Based Denoising of Head Impact Kinematics Measurements With Convolutional Neural Network for Traumatic Brain Injury Prediction](/publication/2024-denoise/)
```

#### Deep Learning Brain Model | 深度学习大脑模型

Path:

```text
content/resources/deep-learning-brain-model/index.md
content/resources/deep-learning-brain-model/featured.jpg
```

Content requirements:

1. English first, Chinese second.
2. Describe computing spatiotemporal brain-strain distributions.
3. Inputs are six-axis head kinematics from wearable devices.
4. Do not mention `braimpact.cn`.
5. Only say to contact us if they want to use it or collaborate.

Related publications:

```markdown
- [Rapid Estimation of Entire Brain Strain Using Deep Learning Models](/publication/2021-mlhm/)
- [Finding the Spatial Co-Variation of Brain Deformation With Principal Component Analysis](/publication/2022-pca/)
- [Brain Deformation Estimation With Transfer Learning for Head Impact Datasets Across Impact Types](/publication/2024-mlhmtwo/)
- [Adaptive Machine Learning Head Model Across Different Head Impact Types Using Unsupervised Domain Adaptation and Generative Adversarial Networks](/publication/2024-mlhmthree/)
- [AI-Based Denoising of Head Impact Kinematics Measurements With Convolutional Neural Network for Traumatic Brain Injury Prediction](/publication/2024-denoise/)
```

#### Brain-RBF

Path:

```text
content/resources/brain-rbf/index.md
```

GitHub:

```text
https://github.com/Yuzhe-Liu-Lab/Brain-RBF
```

Related publication:

```markdown
- [Quantifying Morphology-Related Deviations in Brain Strain Using an Automated Mesh Morphing Method](/publication/2026-yihan-automorph/)
```

#### FE Head Impact Simulations

Path:

```text
content/resources/fe-head-impact-simulations/index.md
```

GitHub:

```text
https://github.com/Yuzhe-Liu-Lab/FE_head_impact_simulations_Public
```

Must include:

```markdown
- [Local and Global Effects of Inertial Force Components Producing Brain Strain During Head Impacts](/publication/2025-inertialforce/)
```

Also include all large-scale brain-strain computation related papers, including MLHM, PCA, CSDM/piecewise, time-window, MPSR, transfer learning, domain adaptation, denoising, and head-impact subtyping papers.

Useful local search:

```powershell
rg -n "brain strain|Brain Strain|head impact|Head Impact|simulation|finite element|inertial force|large-scale|large scale|strain" content/publication -g "index.md"
```

Current related publication list:

```markdown
- [Local and Global Effects of Inertial Force Components Producing Brain Strain During Head Impacts](/publication/2025-inertialforce/)
- [Rapid Estimation of Entire Brain Strain Using Deep Learning Models](/publication/2021-mlhm/)
- [The Relationship Between Brain Injury Criteria and Brain Strain Across Different Types of Head Impacts Can Be Different](/publication/2021-relationship/)
- [Predictive Factors of Kinematics in Traumatic Brain Injury from Head Impacts Based on Statistical Interpretation](/publication/2021-predicitive/)
- [Finding the Spatial Co-Variation of Brain Deformation With Principal Component Analysis](/publication/2022-pca/)
- [Piecewise Multivariate Linearity Between Kinematic Features and Cumulative Strain Damage Measure (CSDM) Across Different Types of Head Impacts](/publication/2022-piecewise/)
- [Time Window of Head Impact Kinematics Measurement for Calculation of Brain Strain and Strain Rate in American Football](/publication/2022-timewindows/)
- [Brain strain rate response: Addressing computational ambiguity and experimental data for model validation](/publication/2023-brain-strain-rate-ambiguity/)
- [Differences between two maximal principal strain rate calculation schemes in traumatic brain analysis with in-vivo and in-silico datasets](/publication/2024-mpsrcal/)
- [Brain Deformation Estimation With Transfer Learning for Head Impact Datasets Across Impact Types](/publication/2024-mlhmtwo/)
- [Adaptive Machine Learning Head Model Across Different Head Impact Types Using Unsupervised Domain Adaptation and Generative Adversarial Networks](/publication/2024-mlhmthree/)
- [AI-Based Denoising of Head Impact Kinematics Measurements With Convolutional Neural Network for Traumatic Brain Injury Prediction](/publication/2024-denoise/)
- [Machine-learning-based head impact subtyping based on the spectral densities of the measurable head kinematics](/publication/2023-classification/)
```

#### Clustering Template for Brain Strain

Path:

```text
content/resources/clustering-template-brain-strain/index.md
```

GitHub:

```text
https://github.com/Yuzhe-Liu-Lab/Clustering-Template-for-Brain-Strain
```

If no related paper is specified, write:

```markdown
- Related publications will be added as they become available.
```

### How To Find Related Publications For Resources

Use several passes.

1. Search by direct keywords:

```powershell
rg -n "mouthguard|instrumented mouthguard|wearable" content/publication -g "index.md"
rg -n "brain strain|machine learning head model|MPSR|CSDM|head impact" content/publication -g "index.md"
rg -n "RBF|morphology|morphing|mesh" content/publication -g "index.md"
```

2. Search by exact repository concept:

```powershell
rg -n "inertial force|six-axis|finite element simulation|head kinematics" content/publication -g "index.md"
```

3. List candidate titles and slugs:

```powershell
@'
from pathlib import Path
import re
root = Path("content/publication")
for p in sorted(root.glob("*/index.md")):
    txt = p.read_text(encoding="utf-8")
    m = re.search(r'^title:\s*"?(.+?)"?\s*$', txt, re.M)
    if m and any(k in txt.lower() for k in ["brain strain", "mouthguard", "machine learning head model", "inertial force"]):
        print(p.parent.name, "=>", m.group(1).strip('"'))
'@ | python -
```

4. Use the `/publication/<slug>/` link. Hugo lowercases paths in output, but source folders may have uppercase characters. Prefer the generated/public URL if unsure.

5. Verify every link exists after build:

```powershell
@'
from pathlib import Path
import re
root = Path(r"D:\Works_ThinkpadT14p\LabWebsite\Sites_team\Yuzhe-Liu-Lab.github.io")
md = (root / "content/resources/fe-head-impact-simulations/index.md").read_text(encoding="utf-8")
for href in re.findall(r'\]\((/publication/[^)]+/)\)', md):
    p = root / "public" / href.strip("/").replace("/", "\\") / "index.html"
    print(href, p.exists())
'@ | python -
```

## GitHub Repository Resources

When the user asks to update Resources from GitHub organization:

```text
https://github.com/orgs/Yuzhe-Liu-Lab/repositories
```

Fetch current repositories:

```powershell
curl.exe -L https://api.github.com/orgs/Yuzhe-Liu-Lab/repos?per_page=100
```

Public repositories at the time of this guide:

```text
Brain-RBF
Yuzhe-Liu-Lab.github.io
Clustering-Template-for-Brain-Strain
FE_head_impact_simulations_Public
```

Do not list the website repository itself as a scientific resource unless specifically asked.

Read repository README:

```powershell
curl.exe -L https://raw.githubusercontent.com/Yuzhe-Liu-Lab/Brain-RBF/main/README.md
curl.exe -L https://raw.githubusercontent.com/Yuzhe-Liu-Lab/FE_head_impact_simulations_Public/main/README.md
```

Use repository descriptions and README text for the English introduction, then write a faithful Chinese introduction.

## Image Handling For Resources

If a resource has a product/device/model image:

1. Place image at:

```text
content/resources/<slug>/featured.jpg
```

2. Let Hugo auto-render it as the page header.
3. Do not manually insert the same image in the markdown body.
4. For product photos, make a horizontal web-friendly image if possible.
5. If adding a more technical look, use subtle overlays, not distracting decorations.

Example image processing with bundled Python and Pillow:

```powershell
@'
from pathlib import Path
from PIL import Image, ImageEnhance, ImageFilter

src = Path(r"C:\path\to\source.jpg")
out = Path(r"D:\Works_ThinkpadT14p\LabWebsite\Sites_team\Yuzhe-Liu-Lab.github.io\content\resources\instrumented-mouthguard\featured.jpg")

img = Image.open(src).convert("RGB")
w, h = img.size
img = img.crop((int(w*0.02), int(h*0.18), int(w*0.98), int(h*0.88)))

target = (1600, 900)
scale = max(target[0]/img.width, target[1]/img.height)
img = img.resize((int(img.width*scale), int(img.height*scale)), Image.Resampling.LANCZOS)
x = (img.width-target[0])//2
y = (img.height-target[1])//2
img = img.crop((x, y, x+target[0], y+target[1]))

img = ImageEnhance.Sharpness(img).enhance(1.3)
img = ImageEnhance.Contrast(img).enhance(1.15)
img.save(out, quality=92, optimize=True)
'@ | & 'C:\Users\Lenovo\.cache\codex-runtimes\codex-primary-runtime\dependencies\python\python.exe' -
```

For more advanced processing, first check that Pillow exists:

```powershell
@'
import PIL
print(PIL.__version__)
'@ | & 'C:\Users\Lenovo\.cache\codex-runtimes\codex-primary-runtime\dependencies\python\python.exe' -
```

## Build And Preview Verification

Preferred verification:

```powershell
hugo --minify --noBuildLock
```

Known benign warning:

```text
WARN skipping template file "...sitemap.xml": unrecognized render hook template
```

This warning has appeared during successful builds and does not by itself mean the build failed.

If the build hangs:

1. Check Hugo processes.
2. Kill only processes created by the current work if possible.
3. Build to a temporary destination:

```powershell
hugo --logLevel info --noBuildLock --destination D:\Works_ThinkpadT14p\LabWebsite\Sites_team\Yuzhe-Liu-Lab.github.io\public-test
```

4. Inspect `public-test`.
5. If needed for immediate preview, copy the relevant generated section from `public-test` to `public`.
6. Delete `public-test` after verification.

Check a local page:

```powershell
Invoke-WebRequest -UseBasicParsing http://127.0.0.1:1313/resources/instrumented-mouthguard/
```

Check that a page contains/does not contain text:

```powershell
try {
  $r = Invoke-WebRequest -UseBasicParsing http://127.0.0.1:1313/resources/deep-learning-brain-model/
  "$($r.StatusCode) contains_braimpact=$($r.Content.Contains('braimpact')) contains_contact=$($r.Content.Contains('please contact us'))"
} catch {
  $_.Exception.Message
}
```

Use browser verification after frontend/content changes that affect layout or images:

1. Open the page in the in-app browser.
2. Confirm expected title, image count, links, and visible bilingual content.
3. For pages with `featured.jpg`, confirm there is only one visible image unless two are intentional.

## Temporary Build Directories

Temporary output directories used during troubleshooting:

```text
public-test
public-resource-test
public-bg-test
```

These are not source. Delete them after use:

```powershell
$root=(Resolve-Path '.').Path
$p=Join-Path $root 'public-resource-test'
$resolved=Resolve-Path -LiteralPath $p -ErrorAction SilentlyContinue
if ($resolved -and $resolved.Path.StartsWith($root)) {
  Remove-Item -LiteralPath $resolved.Path -Recurse -Force
}
```

Only delete temporary directories after confirming the resolved path is inside the repository root.

## Final Checklist Before Reporting Done

For any update:

1. Source files updated, not only `public`.
2. UTF-8 Chinese verified if PowerShell displays mojibake.
3. `hugo --minify --noBuildLock` or temporary Hugo build passes.
4. Generated page exists in `public` or temporary destination.
5. Links resolve.
6. Images exist and are not duplicated.
7. For News: title and body are English first, Chinese second.
8. For Publications: DOI, Source Document, `publication_types: ["Journal"]`, author naming, image before Abstract.
9. For Resources: overview has one-line summary; subpage has English intro, Chinese intro, contact line, related publications.
10. For People: correct group and `entry_year`.
11. If a local preview is running, refresh with `Ctrl + F5` if old CSS or images are cached.

