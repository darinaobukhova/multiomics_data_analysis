# Multi-omics data analysis 

A personal collection of resources, focused on multi-omics data analysis. 

# Relevance 

In the recent years, a plethora of methods capturing multiple modalities, such as RNA expression, DNA methylation, chromatin accessibility and protein abundance among others, from the same cell (hence, single-cell multi-omics) have been developed. Here I will collect papers, methods, tutorials and other things related to the single-cell omics. 

# Review papers

## Methods' general overviews

- [A comprehensive review of single-cell multiomics methods and their use](https://www.cell.com/trends/biotechnology/fulltext/S0167-7799(20)30057-3) by Ma, A., McDermaid, A., Xu, J., Chang, Y., Ma, Q. This review discusses the application of existing single-cell multi-omics tools through two designed case studies and give a summary of current challenges and future perspectives. 
- [A comprehensive review of single-cell multiomics technology and data analysis methods](https://www.nature.com/articles/s12276-020-0420-2#citeas) by Lee, J., Hyeon, D.Y., Hwang, D., Contents-wise similar to the review above, this one also explains the part preceding multi-omics data analysis: cell isolation and barcoding. Moreover, it goes into more details in the double-modality analysis: transcriptome–genome, transcriptome–epigenome, transcriptome–proteome. 


# Analytical methods papers

## Data Integration

#### Challenges in multi-omics data integration:
- Data modalities are collected using different techniques →  exhibit heterogeneous statistical properties;
- Have a lot of missing values → not suitable for classical statistical methods; 
- Can possibly have undesired sources of heterogeneity (technical/unrelevant biological)
- Complexity of the data 

[### MOFA+: a statistical framework for comprehensive integration of multi-modal single-cell data](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-020-02015-1) by Argelaguet, R., Arnol, D., Bredikhin, D., Deloro, Y., Velten, B., Marioni, J.C., Stegle, O.

MOFA+ is an unsupervised statistical framework, designed for the integration of multiple omics modalities via a common sample space (measurements derived from the same set of cells). It is an extension of [MOFA](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6010767/) with additional functionality (e.g., multi-group framework allowing to capture within-group sources of variability) and a faster inference. The method can be viewed as generalization of PCA to multi-omics data. 

**MOFA+ Input**: a several data matrices with measurements of multiple -omics types on the same/overlapping sets of samples. 

**MOFA+ Output**: an interpretable low-dimensional representation in terms of k latent factors (their interpretation is analogous to interpretation of the principle components in PCA) with associated feature weight matrices/data modality, explaining the major axes of variation across the datasets. 

A wide range of downstream analyses, including inspection of feature weights (a measure of the relation between each factor and feature), variance decomposition (quantification of the amount of variance explained by each factor in data modality) and clustering among others, is possible. 

A more comprehensive overview of the method is available by one of its authors, Ricard Argelaguet, as [Youtube Video from VIB training workshop](https://www.youtube.com/watch?v=_BfHeZ0s2i0). My summary of the talk with relevant screenshots is available [here](https://drive.google.com/file/d/1uwlFvaKr3CvyPI5rIA-MIWvDvp2loLgK/view?usp=sharing).

