# An Analysis of Standard Error Estimation for Clustered Data
This repository contains code used to generate the paper [Project.pdf](Project.pdf). 

## Abstract

Clustered data is common in real-world settings and of particular interest to the field of causal inference when working with cluster randomized trials. When performing inference tasks on clustered data, it is critical to account for the inherent grouping structure in standard error estimation, as methods that ignore clustering exhibit severe downward bias. In this project, we first discuss techniques commonly used in the literature to estimate standard errors in clustered data. Then, we perform Monte Carlo simulations with varying numbers of clusters, observations per cluster, and intracluster correlation (ICC) to evaluate the performance of three different bootstrap-based standard error estimation techniques: (1) a standard bootstrap where clustering is ignored, (2) a block bootstrap method where clusters are resampled, and (3) a “double” bootstrap that first resamples by cluster and then performs a standard bootstrap within each resampled cluster. Results from these simulations align with findings in the literature that the standard bootstrap exhibits significant downward bias in the presence of non-zero ICC, and additional trends are also explored. Lastly, these three bootstrap-based standard error estimation techniques are applied to a real-world data set that contains home sale prices in Ames, IA, clustered by neighborhood. While the true population parameter is not known in this case, it is easily observable that the standard bootstrap produces the tightest confidence interval and likely underestimates the degree of uncertainty in the inference task.

## Documents of interest

- `Project.pdf`: Written report, outlining our research, simulations procedure, case study, discussion, and results
- `Project.Rmd` and `Scripts/` files: Code used to generate `Project.pdf`
- `Presentation.pptx`: Slides used to present high-level results

## Acknowledgements

This project was completed as part of STA 640 (Causal Inference) at Duke, taught by Professor Fan Li. I partnered with a classmate, [Rob Kravec](https://github.com/robkravec), on this project.

