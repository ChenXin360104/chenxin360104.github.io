---
title: "OM3: An Ordered Multi-level Min-Max Representation for Interactive Progressive Visualization of Time Series"
authors:
- Yunhai Wang
- Yuchun Wang
- xinchen
- Yue Zhao
- Fan Zhang
- Eugene Wu
- Chi-Wing Fu
- Xiaohui Yu

author_notes:
  - 'Equal contribution'
  - 'Equal contribution'
  - 'Equal contribution'
  - ''
  - ''
  - ''
  - ''

date: "2023-06-20T00:00:00Z"
doi: "10.1145/3589290"

# Schedule page publish date (NOT publication's date).
publishDate: "2023-06-20T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["paper-conference"]

# Publication name and optional abbreviated publication name.
publication: In *ACM SIGMOD/PODS International Conference on Management of Data*
publication_short: In *ACM SIGMOD*

abstract: In this paper, We present a novel multi-level representation of time series called OM3 that facilitates efficient interactive progressive visualization of large data stored in a database and supports various interactions such as resizing, panning, zooming, and visual query. Based on our proposed line-segment aggregation, this representation can produce error-free line visualizations that preserve the shape of a time series in windows of arbitrary sizes. To reduce the interaction latency, we develop an incremental tree-based query strategy to support progressive visualizations, allowing a finer control on the accuracy-time tradeoff. We quantitatively compare OM3 with state-of-the-art methods, including a method implemented on a leading time-series database InfluxDB, in two settings with databases residing either in the local area network or on the cloud. Results show that OM3 maintains a low latency within 300 ms on the web browser and a high data reduction ratio regardless of the data size (ranging from millions to billions of records), achieving around 1,000 times faster than the state-of-the-art methods on the largest dataset experimented with.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Query optimization
- Information visualization
- Time series
- Interactive progressive visualization
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: 'https://www.yunhaiwang.net/sigmod2023/om3/paper.pdf'
url_code: 'https://github.com/Ideas-Laboratory/om3'
url_dataset: ''
url_poster: ''
url_project: 'https://www.yunhaiwang.net/sigmod2023/om3/'
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Our OM<sup>3</sup>-based architecture for interactive progressive error-free visualization of time series stored.'
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

![forward_transformation](transform.png "Illustrating the OM3 forward transform and the coefficients stored in the database. (a) The input data (bottom) with 16 samples is recursively transformed to build the four-level coefficient tree. Each tree node has two aggregate coefficients and two associated detail coefficients. To start, we replicate the input data twice to construct the coefficients at level 4, marked by the dotted box. (b) The initial database table stores the final two aggregate coefficients at the top (level 0) and all detail coefficients from the forward transforms; detail coefficients that are redundant for reconstructing the original data are marked by the blue box. (c) The additional database table stores all ordering coefficients. (d,e) Line visualizations (in black) reconstructed by the inverse transform from the aggregate coefficients on a two-pixel-wide window (d) and a four-pixel-wide window (e), where the pixels with the red boxes are missed.")

![tree_query](tree_query.jpg "Illustrating how incremental tree-based query supports for accurately visualizing a time series on a three-pixel-width window. (a) Simply generating the visualization by using four groups of the aggregate values at the level 2 could easily miss pixels (red boxes). (b,c) Our query method with pruning can efficiently visit necessary nodes in the OM3 coefficient tree to locate the minimum and maximum aggregates for each pixel column in the target window level by level and uses these value ranges to rasterize the pixel columns in (c). (d) The final visualization produced by our method (grey pixels) is error-free; its rasterization precisely matches the data points in the original line chart. Here, the detail coefficients of the node [14,17] do not need to be loaded, since its value range is covered by the value ranges of the adjacent two pixel columns [7,20] and [6,29], while the inter-column line highlighted in (d) corresponds to the node [14,22].")

![progressive_performance](pro_performance.jpg "(a,b) Boxplots summarize the response time of 20 trials for producing visualizations with SSIM values larger than 0.95 after performing three interactions on the two datasets. (c,d) The line charts show how SSIM-based visualization quality evolve over the response time for a randomly selected trial for each interaction on the two data.")

![case_study](om3_teaser.png "44 stock price lines visualized using OM3, exhibiting heavy visual clutter. Hence, we put the timebox marked by the blue box to filter out the stocks with different behaviors and produce the visualization shown in (b). (c) Further, we zoom into a specific time interval between 2019 and 2022 and then use a timebox to further filter the stocks.")

### Supplementary Material
The supplemental material file is available at <https://www.yunhaiwang.net/sigmod2023/om3/supp.pdf>.
