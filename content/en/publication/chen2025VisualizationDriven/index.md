---
title: "Visualization-Driven Illumination for Density Plots"
authors:
- xinchen
- Yunhai Wang
- Huaiwei Bao
- Kecheng Lu
- Jaemin Jo
- Chi-Wing Fu
- Jean-Daniel Fekete

author_notes:
  - ''
  - 'Corresponding author'
  - ''
  - ''
  - ''
  - ''
  - ''

date: "2025-02-01T00:00:00Z"
doi: "10.1109/TVCG.2024.3495695"

# Schedule page publish date (NOT publication's date).
publishDate: "2025-02-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Transactions on Visualization and Computer Graphics"
publication_short: "IEEE TVCG"

abstract: We present a novel visualization-driven illumination model for density plots, a new technique to enhance density plots by effectively revealing the detailed structures in high- and medium-density regions and outliers in low-density regions, while avoiding artifacts in the density field's colors. When visualizing large and dense discrete point samples, scatterplots and dot density maps often suffer from overplotting, and density plots are commonly employed to provide aggregated views while revealing underlying structures. Yet, in such density plots, existing illumination models may produce color distortion and hide details in low-density regions, making it challenging to look up density values, compare them, and find outliers. The key novelty in this work includes (i) a visualization-driven illumination model that inherently supports density-plot-specific analysis tasks and (ii) a new image composition technique to reduce the interference between the image shading and the color-encoded density values. To demonstrate the effectiveness of our technique, we conducted a quantitative study, an empirical evaluation of our technique in a controlled study, and two case studies, exploring twelve datasets with up to two million data point samples.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Density plot
- Illumination
- Shading
- Image composition
featured: true

# links:
# - name: ""
#   url: ""
url_pdf: 'https://www.yunhaiwang.net/tvcg2024/Shaded-Density-Field/paper.pdf'
url_code: 'https://github.com/XinChen-SDU/Visualization-Aware-Illumination-for-Density-Plots'
url_dataset: ''
url_poster: ''
url_project: 'https://www.yunhaiwang.net/tvcg2024/Shaded-Density-Field/'
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Different methods for visualizing two million-point samples of the “New York TLC Trip” dataset (bottom right in (a) shows the raw plot). Our technique is shown in (d). The green box represents a high-density (HD) region, the red box shows a low-density (LD) one, i.e., outliers, and the blue box has medium-density (MD). The HD variations are faithfully revealed in (a,d), but (b,c) hinder the perception of absolute density values by using colors absent from the colormap (brown and blue). On the other hand, LD outliers are revealed in (c,d) and hidden in (a,b). Finally, the MD structures are revealed in (b,c,d) and hidden in (a). Our Visualization-driven Illuminated Density Plot (VIDP) not only shows the density variations using colors similar to (a) but also reveals MD structures and LD outliers.'
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

![parameter_analysis](parameter_analysis.png "Parameter analysis on the Hertzsprung-Russell diagram dataset [31]. (a,b,c,d) Increasing η makes low-density structures more salient while the high-density structures remain unchanged. (e,f,c,g,h) Decreasing φ makes low-density structures clearer, but at the same time darkens high-density structures.")

![quantitative_eval](quantitative_eval.png "Comparison of the degree of color distortion (DCD) produced by four experimental techniques on ten datasets. Dash lines indicate the average DCD of their corresponding techniques. For values out of the plot range, we treat them as outliers and draw a dark halo to indicate them.")

![user_study](user_study.png "Confidence interval plots and statistical tables of the error rate and response time for each task in our user study. Red points indicate the mean values and error bars represent 95% confidence intervals. Each table shows the statistical test results of our experimental techniques, showing the mean with 95% confidence interval and p-value from the Mann-Whitney test against our VIDP technique.")

![SUP_variants_comparison](SUP_variants_comparison.png "Comparing variants of SUP and our VIDP technique using the Barcelona Accidents dataset. (a, b, c) The replicated results of CDP and SUP variants without shading and with Phong shading and ambient occlusion (AO), respectively, as presented in Trautner et al. [4]. (d) The VIDP result with default parameters. According to Equation 8, the degree of color distortion of (b,c,d) are 4.09, 2.24, and 1.27, respectively.")

![case_study_uk](case_study_uk.png "VIDP of the “UK Road Safety” dataset [46] using the Viridis color map and the default parameters. (a) A small local η =0.2 can suppress minor structures in the area above London (the blue box in (b)), and a large local η =20 can reinforce minor structures in the northwest area of Scotland (the red box in (b)).")

### Supplementary Material
The online demo is hosted on <https://xinchen-sdu.github.io/Visualization-Aware-Illumination-for-Density-Plots/>.

The full evaluation results, user study website, and the analysis code are available at [OSF](https://osf.io/5xpsw/?view_only=0445046dad574d4a90d7138e94547ada).