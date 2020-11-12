# LiLab_spatial_transcriptome
codes for Spatial transcriptome analysis by using R Seurat package.
We used Seurat v3.2 package (https://satijalab.org/seurat/) in the R environment to conduct a follow-up study on the RNA count matrix data of ST samples.

## 1. System requirements
- Hardware recommendation: CPU thread >=4, RAM >=16GB
- Common operating systems: Windows, Linux or Mac OS
- R software, version 3.6 or greater.
- Seurat package version 3.2

## 2. Installation guide
1.  Install R, version 3.6 or greater. (https://www.r-project.org/). Install R Studio (Recommended) (https://rstudio.com/)
2.  Installation Instructions for Seurat (v3.2 or greater):
`remotes::install_github("satijalab/seurat", ref = "release/4.0.0")`

## 3. Demo
There is Demo data in the tutorial provided by seurat official website, it is recommended to follow their manual to run.
https://satijalab.org/seurat/spatial_vignette.html

## 4. Instructions for use
Run R code in the .R file: Spatial_transcriptome_analysis_Seurat.R
Make sure your working environment in R and change file paths to your own paths where you place the input and output files
please refer to the R official website Manual for instructions on using the R environment. (https://cran.r-project.org/manuals.html)



## 5. codes for picking representative spots by using Python script
In order to find the marker genes of the 3 myofiber types more accurately, we only extracted part of the most representative spots.
### Extract method
The number of extracted spots is set to 187 (self decided，here is 60% spots of the cluster with the lowest number of spots).
We firstly find the center spots of each cluster based on the UMAP coordinate matrix data, and then use it as the center of the circle to diffuse out and screen the nearest spots until the specified number 187 is reached.

## 5.1. System requirements
- centOS 7
- python 2.7

## 5.2. Installation guide

No installation needed.
Directly run get_representative_spots.py

## 5.3. Demo/Pick_representative_spots
### Input
- 3cluster-group.txt
- 3cluster-UMAP-distance.txt

### Output
- clusterI-rep-spots187.txt

## 5.4. Instructions for use
Change the hard-coded paths in the code to your own paths where you place the input and output files
