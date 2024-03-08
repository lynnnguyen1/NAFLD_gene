# NAFLD_gene
Gene expression analysis of non-alcoholic fatty liver disease (NAFLD) of diabetes patients, a meta-analysis

 ## Author
 Lynn Nguyen
 
 nguyen_l7@denison.edu

 ## Purpose
The overarching research question guiding this study is to provide a meta-analysis to identify gene expression profiling and molecular function pathways associated with the progression of nonalcoholic fatty liver disease (NAFLD), along with the clinical characteristics of diabetes patients from two US databases in 2015 and 2022.

 ## Prerequisites
 - RStudio (version >= 3.0)
 - Packages (available in R): BiocManager (from Bioconductor), DeSeq2, GEOquery, Random Forest and basic R packages. 

 ## Data

 Data are from studies of Subudhi et al., 2022 and Adrent et al., 2015. Data are acessible under GEO database, GSE163211 and GSE49541. Data is retrieved using GEOquery in R. 

 ## Code
 The author use R / Rstudio (version 4.3.3) with Quarto document for their analysis. Code section on this GitHub is updated everytime the author has new updates in their analysis. The lastest code is in the main page, and previous versions of code are in the "code updates" folder. 

 ## Analysis

 Since this is a meta-analysis, we did our best to respect the experiment design and results that the orginal authors discovered. 

### 1. Preprocessing
- Exclude NA values in both gene expression values and phenotype characteristics
- Filter variables that we want to analyze
- Back-transform gene values 

### 2. Gene expression analysis
- DESeq2 package in R for differentially gene expression analysis, with the condition of NAFLD stages (healthy, simple steatosis and NASH) and diabetes status (have or do not have diabetes)
- Threshold for differentially expressed genes is False Discovery Rate of 5% and log2FoldChange > 2 or <-2
- Identify gene symbol using illuminaHumanv4ACCNUM and molecular function pathway using enrichGO
 

 ## Conclusions 
Will be updated soon. 
