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

### Results

![teaser](Figure_1.png "Different methods for visualizing the 'New York TLC Trip' data with two million points.  (a) The scatterplot suffers from overdrawing; overlapping visual marks obscure the major structures.  (b) A density plot using a Gaussian kernel reveals the global patterns, but the high density in the center (\ie Manhattan) hides peripheral local structures in the blue box, while outliers in the red box are missed.  (c) The Sunspot plot better preserves the outliers but cannot reveal local density variations; see,~\eg the blue box.  (d) Splatterplots abstract the density variations in high-density regions, hiding local structures, but show point samples in low-density regions; see the red box.  (e) Our Bi-Scale density Plot (BSP) provides more details in low-density regions and reveals more underlying structures; and (f) The BSP enriched by our default 2D colormap, additionally allows looking up and comparing absolute density values and local density variations.")

![framework](Figure_2.png "Illustrating our unified bin-summarize-transform-decompose-combine framework, where the bin-summarize stage first produces the density field $F$. Then, we can choose to map $F$ to a new density field $I$ by a global transformation or not. After that, we decompose the result into base layer $B$ and detail layer $D$, together with the associated rendering results $V^b$ and $V^d$, respectively.  Finally, $V^b$ and $V^d$ are combined to yield the final plot $V$. The black arrows indicate the common paths for all methods, whereas the colored arrows indicate technique-specific paths.")

![pipeline](Figure_3.png "The bi-scale density-plot enhancement approach, applied to two pipelines, a Gaussian filter on top and our variance-aware filter on the bottom.  First, we bin-summarize the input data and generate the density field $I$ via a logarithmic transform.  Then, we decompose $I$ into the base and detail layers, using our variance-aware filter (bottom path).  Finally, we magnify the detail layer and incorporate it into the base layer to produce the bi-scale density plot (BSP) to better reveal the outliers (see the ones in the red box).")

![experiment_result](Figure_8.png "The experimental tasks and results of each task in our controlled study.  (a) The table shows how five experimental tasks correspond to the abstract tasks and design requirements. (b-f) The results of the controlled study, where we show the confidence interval plots and statistical tables for the tasks. Error bars represent 95\% confidence intervals. Each table shows the statistical test results of our experimental methods, showing the mean with 95\% confidence interval and p-value from the Mann-Whitney test with two target methods (BSP-VF-1D and BSP-VF-2D).")

![case_study](Figure_10.png "Interactive exploration of the \emph{arXiv} dataset with their corresponding bivariate colormaps. (a) Our BSP plot generated  by the original bivariate colormap (b); and (c) improved BSP that shows more structures generated by adjusting the bivariate colormap with more hue in the value range [100,400] (d).")

### Supplementary Material
The full evaluation results, user study website, and the analysis code are available at [OSF](https://osf.io/7qbhe/?view_only=ffe2ab92df354c43b984953e42ce3af0).