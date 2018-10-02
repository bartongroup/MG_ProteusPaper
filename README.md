# Application note on Proteus

This repository contains the R markdown document, the complete R code and all data needed to create the PDF version of the paper, including all the figures. The main R markdown document `proteus.Rmd` is in `doc` directory, while data are in `data` directory.

## Running the code and creating the PDF file

The following command in R (we recommend using RStudio) will create the PDF document and figures.

```
rmarkdown::render("doc/proteus.Rmd")
```

The following R libraries are required to build the document: knitr, ggplot2, ggdendro, viridis, cowplot and dplyr. Also, the package descibed in this document, *Proteus* is needed. *Proteus* can be installed from [GitHub](https://github.com/bartongroup/Proteus).

## Description of data files

- `sel3data.RData` - binary file containing the selection of 3+3 replicates for the Section `Simple data set`. The file contains two objects: `selevi` and `selmet`, with evidence and metadata, respectively.
- `seltab_n3.txt` - tab-delimited text file with the protein intensities created from the 3+3 replicate data. This is the actual data set used for comparing *Proteus* and *Perseus*. This file was created to be read and processed by *Perseus*.
- `perseus_n3_test_results.txt.gz` - results from *Perseus* used on the simple 3+3 replicate data.
- `protein_stats.RData` - binary file containing statistical properties of the large 35+35 replicates set (full data not released yet).
- `gdat_n3.txt.gz` and `gdat2_n3.txt.gz` - generated data sets used for benchmarking in section `Simulated data set`. They corresponds to data with any number of replicates and at least 2 good replicates, respectively.
- `perseus_gdat_n3_test_results.txt.gz` and `perseus_gdat2_n3_test_results.txt.gz` - results from *Perseus* using simulated data.
