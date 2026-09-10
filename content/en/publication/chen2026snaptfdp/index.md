---
title: "SNAP-tFDP: Massively Scalable Graph Layouts via Sparse Negative Sampling"
authors:
- xinchen
- Shuowei Hou
- Yifan Wang
- Mingliang Xue
- Zezheng Feng
- Oliver Deussen
- Weidong Huang
- Yunhai Wang

author_notes:
- ''
- ''
- ''
- ''
- ''
- ''
- ''
- 'Corresponding author'


date: "2026-08-05T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2026-08-05T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["paper-conference"]

# Publication name and optional abbreviated publication name.
publication: "IEEE VIS 2026"
publication_short: "IEEE VIS"

abstract: >-
  Force-Directed Placement (FDP) is a widely used approach for network
  visualization, yet scaling it to massive graphs while preserving clear
  community structures remains a major computational and visual challenge.
  Existing approximation methods often rely on auxiliary data structures (e.g.,
  spatial trees), which introduce substantial memory overhead; furthermore,
  traditional power-function-based forces frequently fail to separate dense
  clusters effectively. In this paper, we present a negative sampling-based
  algorithm that achieves O(|E|) time complexity with a low memory footprint,
  without requiring complex multi-level representations. In a first step, we
  introduce a linearly normalized degree-weighting scheme, which, combined with
  short-range bounded t-distribution forces, effectively untangles dense
  structures and enhances visual cluster separation. To optimize for this
  formulation efficiently, we introduce an edge-centric negative sampling
  strategy that naturally reconstructs the global degree-weighted objective.
  Furthermore, we design a lock-free, bundle-based parallelization scheme that
  leverages the sparsity of stochastic updates to achieve significant speedups
  while mitigating access conflicts. Comprehensive evaluations on 12
  large-scale graphs demonstrate that the proposed method outperforms
  state-of-the-art algorithms in neighborhood preservation and cluster
  separation. Compared to existing baselines, our method reduces memory
  consumption by 72% on average and leverages simple GPU parallelism to
  generate a high-quality layout for a graph with 4 million nodes and 34
  million edges in below 10 seconds.

tags:
- Graph Layout
- Network visualization
- Negative Sampling
featured: true

url_pdf: 'https://www.yunhaiwang.net/vis2026/SNAP-tFDP/files/paper-snap-tfdp.pdf'
url_code: 'https://github.com/Ideas-Laboratory/SNAP-tFDP'
url_dataset: 'https://osf.io/dtxa5/files/osfstorage'
url_poster: ''
url_project: 'https://www.yunhaiwang.net/vis2026/SNAP-tFDP/'
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: >-
    Iterative layouts of communities with more than 800 users in the
    Orkut online social network (a graph with 259,019 nodes and 6,893,156
    edges) generated using our negative sampling-based graph layout algorithm
    using t-forces, which runs in O(|E|) time. Node colors indicate
    community membership. The initial node positions are obtained using Pivot
    MDS (PMDS) (a), followed by layouts after 1 (b), 5 (c), and 30 (d)
    epochs of the algorithm. The entire layout process required 5.69 seconds
    with 16 CPU threads (120 MByte RAM), whereas DRgraph required 55.64
    seconds on the same settings.
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
projects: []

# Slides (optional).
slides: ""
---

### Results

![fig2](fig2.jpg "Comparison of classical spring-electrical models and t-FDP models with different weighting schemes.")

![fig3](fig3.jpg "Comparison of different degree-weighting schemes for (a) two high-degree nodes and (b) a high-degree node and a low-degree node. The attractive force F<sup>a</sup><sub>t-FDP</sub> is identical in all cases and is shown as a black solid line. Product-based weighting (orange) produces overly strong relative repulsion and its normalized variant (purple) nearly eliminates repulsion for low-degree nodes, while linearly normalized degree weighting (red) provides effective balance.")

![fig4](fig4.jpg "Validation of the edge-centric negative sampling strategy. (a) Energy loss curves showing that the actual energy of SNAP-tFDP converges consistently with the effective energy. (b) Superimposition of layouts by SNAP-tFDP (colored) and the full computation (gray).")

![fig5](fig5.jpg "Effect of the number of negative samples k. (a) Layout results and corresponding runtime of the serial SNAP-tFDP algorithm for different k on the APH dataset. (b) NP, SI, and CQ scores under varying k. Results for individual datasets are shown in gray, with the average across datasets highlighted in red.")

![fig6](fig6.jpg "(a) Convergence of the silhouette index (SI) for the serial SNAP-tFDP algorithm and its two lock-free parallel variants on the largest com-lj graph, where semi-transparent points indicate the results of five independent runs. (b) Layouts at four different epochs; for clarity, only the top 20 largest communities are shown.")

![fig7](fig7.jpg "Heatmaps employing a pink-to-green colormap illustrate the scores of NP (a), SI (b), and CQ (c) for layouts generated by nine methods across all datasets. Empty cells indicate that the graph was too large to be processed by the corresponding method. Each row corresponds to a dataset, and each column to a layout method. Colors are scaled row-wise based on the best and worst within each dataset.")

![fig8](fig8.jpg "Layouts and corresponding runtimes of twelve serial methods for the aircraft dataset. SNAP-tFDP (lower right) combines degree weighting with t-forces, yielding clear cluster structures with the lowest runtime, as fast as pure Pivot MDS.")

![fig9](fig9.jpg "(a) Differences in visual quality scores between the two parallel variants and the serial SNAP-tFDP across all datasets. (b) Speedup comparison of SNAP-tFDP and the parallel implementations of existing methods as a function of the number of CPU threads on the largest com-lj dataset.")

![fig10](fig10.jpg "Figure 10: Runtime of eight layout methods, together with the GPU implementations of FA2, t-FDP, and SNAP-tFDP, across all datasets.")

![fig11](fig11.jpg "Figure 11: Visualization of the com-friendster dataset, containing over 65.6 million nodes and 1.8 billion edges.")

### Supplementary Material
The supplemental material file is available at <https://www.yunhaiwang.net/vis2026/SNAP-tFDP/files/supp-snap-tfdp.pdf>.

### Acknowledgements

The authors like to thank the anonymous reviewers for their valuable input. This work is supported by the grants of the NSFC (No.62402284, No.6260072651, No.U2436209), the Beijing Natural Science Foundation (L247027), NSF of Shandong province (ZR2024QF212), the Liaoning Revitalization Talents Program (No. XLYCE2504024), Liaoning Provincial Doctoral Start-up Research Fund (No. 2026-BS-0096), the Fundamental Research Funds for the Central Universities, and the Research Funds of Renmin University of China.