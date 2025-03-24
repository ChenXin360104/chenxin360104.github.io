---
title: "Palettailor: Discriminable Colorization for Categorical Data"
authors:
- Kecheng Lu
- Mi Feng
- xinchen
- Michael Sedlmair
- Oliver Deussen
- Dani Lischinski
- Zhanglin Cheng
- Yunhai Wang

author_notes:
  - ''
  - ''
  - ''
  - ''
  - ''
  - 'Co-corresponding authors'
  - 'Co-corresponding authors'

date: "2021-01-01T00:00:00Z"
doi: "10.1109/TVCG.2020.3030406"

# Schedule page publish date (NOT publication's date).
publishDate: "2021-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Transactions on Visualization and Computer Graphics"
publication_short: "IEEE TVCG"

abstract: We present an integrated approach for creating and assigning color palettes to different visualizations such as multi-class scatterplots, line, and bar charts. While other methods separate the creation of colors from their assignment, our approach takes data characteristics into account to produce color palettes, which are then assigned in a way that fosters better visual discrimination of classes. To do so, we use a customized optimization based on simulated annealing to maximize the combination of three carefully designed color scoring functions&#58; point distinctness, name difference, and color discrimination. We compare our approach to state-of-the-art palettes with a controlled user study for scatterplots and line charts, furthermore we performed a case study. Our results show that Palettailor, as a fully-automated approach, generates color palettes with a higher discrimination quality than existing approaches. The efficiency of our optimization allows us also to incorporate user modifications into the color selection process.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Color Palette
- Discriminability
- Multi-Class Scatterplot
- Line Chart
- Bar Chart
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: 'https://www.yunhaiwang.net/infoVis2020/palettailor/pdf/vis20a-sub1326-i6.pdf'
url_code: 'https://github.com/IAMkecheng/palettailor'
url_dataset: ''
url_poster: ''
url_project: 'https://www.yunhaiwang.net/infoVis2020/palettailor/color-palette-generation.html'
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Results for different types of categorical data visualizations: (left) Palettailor versus Colorization [6]; (center) Palettailor versus Tableau [30]; (right) Palettailor versus Colorgorical [10]. Our system integrates the creation and the assignment of colours to a visualization in a data-aware manner.'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

{{% callout note %}}
Click the *Cite* button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /callout %}}

{{% callout note %}}
Create your slides in Markdown - click the *Slides* button to check out the example.
{{% /callout %}}

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/).
