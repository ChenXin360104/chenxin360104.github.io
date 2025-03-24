---
title: "Bi-Scale Density-Plot Enhancement Based on Variance-Aware Filter"
authors:
- Huaiwei Bao
- xinchen
- Kecheng Lu
- Chi-Wing Fu
- Jean-Daniel Fekete
- Yunhai Wang

author_notes:
  - ''
  - ''
  - ''
  - ''
  - ''
  - 'Corresponding author'

date: "2025-02-09T00:00:00Z"
doi: "10.1016/j.cag.2025.104180"

# Schedule page publish date (NOT publication's date).
publishDate: "2025-02-09T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: Computers & Graphics
publication_short: CAG

abstract: We present Bi-Scale density Plot (BSP), a new technique to enhance density plots by efficiently optimizing the local density variance in high- and mid-density regions while providing more details in low-density regions.  When visualizing large and dense discrete point samples, scatterplots and thematic maps are often employed and we need density plots to further provide aggregated views. However, in the density plots, local patterns such as outliers can be filtered out and meaningful structures such as local density variations can be broken down. The key innovations in BSP include (i) the unified bin–summarize–decompose–combine framework for interactively bi-scale enhancing density plots through combining large- and small-scale density variations; and (ii) the variance-aware filter, which is reformulated based on the edge-preserving image filter, for maintaining the relative data density while reducing the excessive variability in the density plot. Further, BSP can be adopted with a 2D colormap, allowing simultaneous exploration of the enhanced structures and recovering the absolute aggregated densities to improve comparison and lookup tasks. We empirically evaluate our techniques in a controlled study and present two case studies to demonstrate their effectiveness in exploring large data.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Density plot
- Bi-scale
- Bin–summarize–smooth
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: ''
url_code: 'https://github.com/catbao/Filter-basedDensityMapEnhancement'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Graphical abstract'
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
