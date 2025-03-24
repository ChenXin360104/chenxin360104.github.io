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

{{% callout note %}}
Click the *Cite* button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /callout %}}

{{% callout note %}}
Create your slides in Markdown - click the *Slides* button to check out the example.
{{% /callout %}}

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/).
