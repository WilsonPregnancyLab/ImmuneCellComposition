# Distinct DNA Methylation Signatures in Maternal Blood Reveal Unique Immune Cell Shifts in Preeclampsia and the Pregnancy-Postpartum Transition: Associated Code

This study aims to identify and characterize changes in immune cell composition in preeclampsia using two publicly available DNA methylation datasets of maternal blood from normotensive and preeclamptic pregnancy. The scripts used in our analysis are described below.

## GSE37722-GSE192918_EpiDISH_Quantiles.Rmd
This R Markdown script downloads both GSE37722 and GSE192918 datasets from GEO using GEOQuery, merges them by methylation probe ID, and performs quantile normalization. The EPIDish package for R is used for immune cell deconvolution, creating in immune cell proportion data for analysis. A stacked bargraph (*NvPE_stacked_bar_plot.png* in the `plots` subdirectory) produced using the ggplot2 package for R illustrates the differences in overall immune cell composition between the normotensive and preeclamptic pregnancy, with a Kolmogorov-Smirnov test assessing differences in composition distribution. Individuals paneled plots show the difference in cell type proportion between normotensive and preeclamptic pregnancy (*PEvsNorm.png* in the `plots` subdirectory), using a Wilcoxon test to assess differences in the average proportion between the two conditions.
## GSE192918_GestationalAgeImmunocomp.Rmd
This R Markdown script downloads the GSE192918 dataset from GEO using GEOQuery and performs immune cell deconvolution using the EPIDish package. Cell type proportions are then stratified by pregnancy timepoint (see preprint). A stacked bargraph is produced using ggplot2 to show changes in immune cell composition across gestation, with an Anderson-Darling All-Pairs Comparison test being used to assess statistical differences between timepoints (*GSE192918_Temporal_stacked_bar_plot.png* in the `plots` subdirectory). A linear model using the limma package for R is then used to assess differences in individual cell type proportions across gestation (*GSE192918_Timepoint.png* in the `plots` subdirectory).
## GSE37722_GestationalAgeImmunocomp.Rmd
This R Markdown script follows the same set of steps as **GSE192918_GestationalAgeImmunocomp.Rmd** but uses data from GSE37722 and produces the stacked bargraph *GSE37722_Temporal_stacked_bar_plot.png* and individual cell type proportion plot *GSE37722_Timepoint.png*.
#
A preprint for this work can be found below:

*Distinct DNA Methylation Signatures in Maternal Blood Reveal Unique Immune Cell Shifts in Preeclampsia and the Pregnancy-Postpartum Transition*  
Laiba Jamshed, Keaton W. Smith, Samantha L. Wilson  
bioRxiv 2024.12.13.628167; doi: https://doi.org/10.1101/2024.12.13.628167
