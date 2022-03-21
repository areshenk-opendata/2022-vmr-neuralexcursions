# 2022-vmr-neuralexcursions

This repository contains example data and tutorial files for the analyses reported in Areshenkoff et al. (2022). It includes three rmarkdown files describing the covariance centering, manifold excursion, and joint embedding reported in the manuscript.

## Data

The `data/` folder contains two files. The file `example_data.rds` contains a dataframe with columns for subject, scan type (rest and task), and data (containing TR x ROI matrices of standardized BOLD activation data). The file `atlas_cognitive_network.csv` contains information about each ROI.

## Tutorial files

The `Rmd/` folder contains three Rmarkdown files:

- __01-covariance_centering__: Contains a detailed walkthrough, with example code, of the covariance centering procedure used in the manuscript.
- __02-manifold_excursion__: Computes resting state manifold excursion and implements a functional PCA of subject excursion curves.
- __03-covariance_embedding__: Performs a joint embedding of the centered covariance data computed in `01-covariance_centering`

Note that the embedding itself is performed using the code provided by Wang et al. (2017), and published in a repository at https://github.com/shangsiwang/Joint-Embedding. As the code is not released with any open license, the script is not included here. It can be downloaded from the linked repository and placed in the `R/` subdirectory.

The compiled html files are included in the `guides/` directory.

## Required packages

Running all three tutorial files requires the following packages: `fda`, `ggplot2`, `irlba`, `MASS`, `Matrix`, `plyr`, `proxy`, `RColorBrewer`, `zoo`, and (of course) `rmarkdown`.

The user will also require the `spdm` packages, which can be found in a repository at: https://github.com/areshenk-rpackages/spdm
