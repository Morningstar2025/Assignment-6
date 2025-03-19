# Assignment-6
Completed
---
title: "Assignment 6"
author: "Angela Dillon"
date: "`r Sys.Date()`"
output: pdf_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

# Exploring R Packages: `heatmaply`
Fish 549 - Best Practices in Environmental Data Science

## Package Title
`heatmaply` package can be installed from CRAN and GitHub:

* [CRAN](https://cran.r-project.org/package=heatmaply)

* [Github](https://github.com/talgalili/heatmaply)

To install:
```{r}
install.packages("heatmaply")
```

or the latest development version from GitHub:
```{r}
devtools::install_github("talgalili/heatmaply")
```

## Vignette(s)

The package includes a vignette titled **Introduction to heatmaply** available via:
```{r}
vignette("heatmaply")
```

This vignette provides an overview of interactive heatmaps, customization options, and examples for clustering, color mapping, and dendrogram adjustments. 

## Applications 
I found an example on Stack Overflow for visualizing Iris sepal length and width and petal length and width in various countries. 

The National Cancer Institute used `heatmaply` to show incidence rates for cancer in Maryland for all ages, sexes, and races between 2014-2018. 

An article on the Environmental impact and mobility of thallium and other metal(oid)s in soils near a decommissioned Zn-Pb mine used `heatmaply` to show a clustermap of major and trace element total concentrations in samples. 

Testing: 
```{r}
library(heatmaply)
heatmaply_cor(
  cor(mtcars),
  xlab = "Features",
  ylab = "Features",
  k_col = 2,
  k_row = 2
)

```


## Review of `heatmaply`

The primary purpose of `heatmaply` is to create interactive heatmaps in R, using the plotly library for visualization. It extends base R's heatmap functions with custom clustering, color scaling, and hierarchical dendrogram options. 

The `heatmaply` package is widely used for:

* Exploring correlations in environmental data sets
* Comparing species abundance across ecosystems
* Visualizing gene expression data in bioinformatics
* Financial risk analysis

Several applications and tutorials can be found on 
* R-bloggers
* GitHub repo examples
* YouTube

### Pros
-Interactive and user friendly: Unlike static heatmaps, `heatmaply` allows users to zoom, hover, and pan across the map.

-Customizable clustering: Offers hierarchical clustering with different distance metrics. 

-Publication ready graphics: Works well for reports and presentations.

-Compatible: Works with Shiny, R Markdown, and HTML

### Cons 

-Not great with large data sets. 

-Steep learning curve.

# Recommendation:

No. It looks cool. It's interactive, which is always more fun.The graphs remind me of the waffle plots, which are easy to interpret quickly. I think this could be great since I wouldn't have to load my data into ArcGIS Pro or other software, but it's missing the spatial component. I love GIS because you get the location information which helps to orient your reader. 

