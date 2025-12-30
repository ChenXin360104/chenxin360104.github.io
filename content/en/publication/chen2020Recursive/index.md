---
title: "A Recursive Subdivision Technique for Sampling Multi-class Scatterplots"
authors:
- xinchen
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
featured: true

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

### Results

![parameter_analysis](param_analysis.png "Parameter analysis for our method on the Person Activity data set. (a,b,c) Grid size inﬂuences the number of point samples. From left to right, the results have 5969, 2273, and 1217 points, respectively. (d,e,f) For a large λ, many outliers become visible, but overdraw happens in dense areas, while a small λ reduces overdraw but miss a few outliers. (g,e,h) A large τ shows too many outliers and regions of medium density are suppressed, while a small τ is more balanced but outliers are reduced. (i) When λ and τ both are large, the overdraw issue becomes severe while showing many outliers.")

![quantitative_comparison](quantitativecmpr.png "Boxplots summarizing the scores of four measures for four sampling methods over all tested datasets: (a) PDDr and (b) PCDr, where a higher score indicates better sampling for both measures; (c) ESRr and (d) ECSr, where a lower score indicates better sampling.")

![time_comparison](time.png "(a) Runtimes of the four sampling methods on all datasets; (b) relationship between runtime and sampled points on a synthesized dataset (250K points) (logarithmic scale).")

![case_study_synthetic](case_syn.png "Sampled results of the synthetic dataset with 250K points. (a) original scatterplot (left) and four classes sampled individually (right), the transparency of each point is proportional to its density value; (b,c,d,e)results for 6K points generated by random sampling, non-uniform sampling, blue noise sampling, and our method.")

![case_study_mnist](case_mnist.png "Sampled result of the MNIST dataset: (a)original scatterplot with 70K data points; (b,c,d) sampled results generated by random sampling, non-uniform sampling and our method.")

![case_study_power_comsuption](case_power.png "Exploration of the power consumption dataset with 1,570K data points: (a) the original scatterplot; (b) the sampled result generated by our method.")

### Supplementary Material
The supplemental material file is available at <https://www.yunhaiwang.net/infoVis2019/scatterplot/sampling_supp.pdf>.

High-quality versions of the figures in our paper are available at <https://www.yunhaiwang.net/infoVis2019/scatterplot/sampling_resources.zip>.