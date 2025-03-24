---
title: "A Recursive Subdivision Technique for Sampling Multi-class Scatterplots"
authors:
- Xin Chen
- Tong Ge
- Jian Zhang
- Baoquan Chen
- Chi-Wing Fu
- Oliver Deussen
- Yunhai Wang

author_notes:
  - 'Joint first authors'
  - 'Joint first authors'
  - ''
  - ''
  - 'Co-corresponding authors'
  - ''
  - 'Co-corresponding authors'

date: "2020-01-01T00:00:00Z"
doi: "10.1109/TVCG.2019.2934541"

# Schedule page publish date (NOT publication's date).
publishDate: "2020-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Transactions on Visualization and Computer Graphics"
publication_short: "IEEE TVCG"

abstract: We present a non-uniform recursive sampling technique for multi-class scatterplots, with the specific goal of faithfully presenting relative data and class densities, while preserving major outliers in the plots. Our technique is based on a customized binary kd-tree, in which leaf nodes are created by recursively subdividing the underlying multi-class density map. By backtracking, we merge leaf nodes until they encompass points of all classes for our subsequently applied outlier-aware multi-class sampling strategy. A quantitative evaluation shows that our approach can better preserve outliers and at the same time relative densities in multi-class scatterplots compared to the previous approaches, several case studies demonstrate the effectiveness of our approach in exploring complex and real world data.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- scatterplot
- multi-class sampling
- kd-tree
- outlier
- relative density
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: 'https://www.yunhaiwang.net/infoVis2019/scatterplot/sampling.pdf'
url_code: 'https://github.com/Ideas-Laboratory/RecursiveSubdivision-basedSampling'
url_dataset: ''
url_poster: ''
url_project: 'https://www.yunhaiwang.net/infoVis2019/scatterplot/'
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Different sampling methods for presenting the four-class Person Activity data [8]. (a) The left shows the input scatterplots with 100K points and the right shows the four classes separately, where the patterns of each class are obscured in the main plot, e.g., the three sub-clusters in the purple class, due to overdraw. We re-sample the data into ∼5000 points using (b) random sampling, (c) non-uniform sampling [4], (d) multi-class blue noise sampling [11], and (e) our method. The results show that our method better preserves major outliers (see the rounded boxes labeled with “1”), relative data densities (see the ellipse labeled with “2” to compare (c) with (d)), and the relative class densities (see the orange points shown in the squares labeled with “3” in (a)-(e)), without introducing obvious visual artifacts such as highlighted by the square in (d) labeled with “4”. Points for all results are rendered in random order.'
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
