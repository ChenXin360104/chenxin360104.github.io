---
title: "Visualization-Oriented Progressive Time Series Transformation"
authors:
- xinchen
- Lingyu Zhang
- Huaiwei Bao
- Wei Lu
- Eugene Wu
- Xiaohui Yu
- Yunhai Wang

author_notes:
  - ''
  - ''
  - ''
  - ''
  - ''
  - ''
  - 'Corresponding author'

date: "2025-08-24T00:00:00Z"
doi: "10.1145/3769841"

# Schedule page publish date (NOT publication's date).
publishDate: "2025-12-05T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["paper-conference"]

# Publication name and optional abbreviated publication name.
publication: In *ACM SIGMOD/PODS International Conference on Management of Data*
publication_short: In *ACM SIGMOD*

abstract: Visual analysis of large time-series data often requires transformations over multivariate time series. Existing methods struggle to meet interactive response time requirements, relying on full transformations that incur high computation costs. We propose a visualization-oriented transformation system PIVOT that incrementally generates accurate visualizations by selectively transforming only essential data samples. At its core is a *transformation-aware query mechanism* that efficiently computes point-wise transformations by leveraging cached hierarchical data on the server. To support responsive interaction, we introduce a *pixel-based error-bound guarantee* that estimates the accuracy of intermediate visualizations without requiring a reference, enabling a balance between latency and visual fidelity. Experiments show that PIVOT achieves highly accurate visualizationswith interactive responsetimes, outperforming existing error-free methods by up to an order of magnitude on billion-scale datasets.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Query optimization
- Information visualization
- Time series
- Interactive progressive visualization
- Transformation
featured: true

# links:
# - name: ""
#   url: ""
url_pdf: 'https://www.yunhaiwang.net/sigmod2026/PIVOT/paper.pdf'
url_code: 'https://github.com/ChenXin360104/PIVOT'
url_dataset: ''
url_poster: ''
url_project: 'https://www.yunhaiwang.net/sigmod2026/PIVOT/'
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Overview of our system PIVOT for exploring compressed large-scale time series on a remote server.'
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

![use_case](use_case.png "Visual analysis of multiple time series from a dataset of NYSE-listed stocks. Analysts may casually apply and compose various point-wise transformations to explore interesting patterns, expecting timely and highly accurate visualizations.")

![TAT_illustration](MMH_illustration.png "Illustration of M4 and our proposed TAT representation with a sample time series in (a). (b) The corresponding line charts with two pixel columns: the blue line connects all data points, while the black line uses only M4-aggregated samples in each pixel column. (c) The corresponding TAT structure, where each node stores the minimum and maximum values and the associated time interval.")

![func_class](func_class.png "Illustration of how our solution handles three types of transformation functions: (a) monotonic univariate, (b) non-monotonic univariate, and (c) bivariate. In all cases, the input time series has values {7, 8, 10, 6}, represented by black dots within a single pixel column. The corresponding function values are shown as black squares, while yellow and green squares mark the minimum and maximum function values within the domain, respectively. In (c), an additional time series {4, -3, 0, 1} is used, and the corresponding TAT structures are illustrated in (d).")

![query_mechanism](query_mechanism.png "Illustration of the query mechanism Q on a time series of length 64 over a canvas with three pixel columns. (a) For the non-monotonic function f(x) = (x<sup>2</sup> - 1) / 2, Q retrieves aggregated values from the TAT, with node scores shown below. (b) Evolution of candidate lists α and 𝛽 over the query process, alongside corresponding progressive visualizations. The ground truth f(X), shown in gray, is for reference only; it is not computed during execution.")

![error_bound_estimation](error_bound_estimation.png "Illustration of pixel errors under different combinations of R<sub>k</sub> and gR. (a-d) The four extreme rasterization cases and (e) our average estimation approach using α and 𝛽 values obtained in the first iteration. Red and blue boxes indicate erroneous pixels relative to the final visualization in Figure 5 (b) and consistently rasterized pixels across all four cases, respectively. Black dashed lines serve as virtual guides for rasterization between R<sub>k</sub> that do not correspond to valid results.")

![individual_func_eval](individual_func.png "Performance comparison of three systems using 13 representative transformation functions covering univariate, bivariate, and multivariate cases evaluated on all datasets: (a) SSIM, (b) response time, and (c) memory usage.")

![varying_m_n](varying_m_n.png "Response time (a,c) and memory usage (b,d) of the three systems under varying (a,b) numbers of data points and (c,d) numbers of input variables when applying the transformation L<sub>2</sub><sup>ln</sup>(X) to the synthesized time-series datasets.")

![varying_width](varying_width.png "Results of evaluation metrics on the largest real-world dataset <i>Power</i> as the canvas width varies: (a) SSIM scores and (b) response time.")

![varying_tau](varying_tau.png "Performance under varying pixelerror rate thresholds 𝜏. (a) The boxplots summarize the SSIM scores across all datasets. (b) The dot plot shows the relationship between pixel error rate upper bound ε and the actual pixel rate 𝜁 on the <i>Power</i> dataset. (c) The dot plot displays the mean SSIM scores for various configurations with a fixed 𝜏 = 5%.")

![interactive_comparison](interactive_comparison.png "Interactive performance on the real-world dataset <i>Taxi</i> (a, b) and synthetic dataset <i>Syn5B</i> (c, d): (a, c) SSIM scores; (b, d) response times.")

### Supplementary Material
The supplemental material file is available at <https://www.yunhaiwang.net/sigmod2026/PIVOT/supp.pdf>.