# Alzheimers_GWAS_1Mb_genes_list
This is the R code used to extract gene names within +-500kb of all known Alzheimer's disease SNPs passing genome-wide significance. All loci from the most recent GWAS meta-analysis to date, [Bellenguez et al., 2020](https://www.medrxiv.org/content/10.1101/2020.10.01.20200659v2.full-text), plus APOE rs429358 are considered. The following steps are performed:
1. A dataframe is created with the list of loci, and chromosome positions +-500kb are calculated (total region size is 1Mb for each locus)
2. biomaRt is used to extract all gene names within in each 1Mb region to iteratively add to a final comprehensive dataframe
Note that the purpose of this project is to supplement a single-nucleus RNA-seq experiment (10X Genomics), and therefore ensembl98 is used to be compatible with output from 10X Genomics CellRanger v4 software. This code may be of interest to anyone investigating underlying regulatory mechanisms for Alzheimer's disease.  
