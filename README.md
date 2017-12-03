# Project Portfolio
### *Bram Stone*
[Academic CV](https://github.com/bramstone/bramstone.github.io/blob/master/Curriculum%20Vitae.pdf)

## *Data Exploration*

### Mapping, Visualization, and Data Exploration: US Coal Production
[Repository](https://github.com/bramstone/US-Coal-Production), [Project Narrative (Rmarkdown)](https://github.com/bramstone/US-Coal-Production/blob/master/project_narrative.md)  
This project utilizes the `ggplot`, `maps`, and the `chloroplethr` R packages.

Visualization and mapping of trends in coal mining in the United States from 2000 to 2016. Raw data were obtained in `txt` files from the **Mine Safety and Health Administration (MSHA)**, which is under the US Department of Labor. This project demonstrates trends in coal over several decades, identifying patterns in production and employment. These data are intended to be integrated into a larger EPA dataset linking environmental and economic variables together, and are used in another project to build a predictive model frequency of mining-related accidents.

## *Predictive Modeling*

## *Statistical Programming*

### Creating Ecological Networks Microbial Community Datasets
[Repository](https://github.com/bramstone/Selecting-associations-in-microbial-datasets), [Project Vignette (pdf)](https://github.com/bramstone/Selecting-associations-in-microbial-datasets/blob/master/Vignette.pdf)  
This project utilizes the `vegan` package and is meant to be used to create network graphs with the `igraph` package in R.

The function in this project is an implementation of Lallich et al.'s 2006 algorithm to reduce type I error (the false discovery rate) by selecting a subset of correlations with values deemed suitable or interesting by the researcher. The function writes its output in a data frame format suitable for graphing with the igraph package. Currently, work is being done to incorporate other methods for controlling false discovery.  
[Lallich, S, O Teytaud, E Prudhomme. *Association rule interestingness: measure and statistical validation.* Hamilton, G (ed.) Quality measures in data mining. 2006. Springer.](https://hal.inria.fr/file/index/docid/113594/filename/lal.pdf)

### Quantifying Species Shared Between Microbial Communities
[Repository](https://github.com/bramstone/raup_crick)  
This projet utilizes the `wrswoR` package for weighted resampling without replacement, and the `parallel` and `foreach` packages for parallel computation In R.

The function in this project is an re-implementation from Chase's 2011 paper on calculating probabilistic species sharing patterns between communities using Raup-Crick associations. The original code provided by Chase utilized several nested `for` loops which have been vectorized and a framework for parallel computation has been added (although this will only work on Windows machines). In addition, this function performs weighted resampling without replacement using the `wrswoR` package which is faster than base R's function to accomplish the same task. These changes combine to provide a significant speed-up for large datasets often encountered in microbial ecology. A similar function `raupcrick` exists in the `vegan` package, but this often fails for species-rich microbial datasets.
