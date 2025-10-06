# myrepo
this is a project for bioinfo
This repo is a demonstration of using Git with RStudio. 

# part-1

#Rmd — Gene Expression and Growth Analysis

Purpose

This script is a form of exploratory analysis of gene expression (job ENSG gene IDs) and tree growth (two sites northeast and southwest) data. It illustrates the fundamentals of data management, summary statistics, visualization and statistical testing in R. The important tasks to be performed are Reading and downloading tabular/csv data.
Computing averages of gene expression, finding top-expressing genes, counting low-expressing genes, and distributions.
Computing site-specific means/standard deviations of tree circumference, plotting growth using boxplots, computing 10-year growth, and doing t-test to compare sites.

Main Steps

1 Data Download & Import
Loads the TSV and CSV files on GitHub and downloads them.

2 Gene Expression Analysis
Performs the calculation of average expression of genes in samples.
Determines 10 most highly expressed genes.
Filter counts with a mean expression of less than 10.
Shows a histogram of distribution of gene expression.

3 Tree Growth Analysis
Determines mean and standard deviation of circumference/ site/ year.
Plots boxplots of inter-site growth comparisons.
Calculates the annual growth of each tree.
Conducts t-test to determine whether there is any difference in growth between sites.

Inputs

gene_expression.tsv Gene expression data which includes gene ID and expression of a gene in many samples.

growth_data.csv- Tree growth measurements (circumference) of two locations obtained between 2005 and 2020.

Outputs

Data frames: genedata, growthdata (data with added meanexpression column and growth10yr column).

Tables: Head of datasets, top 10 genes by means of expression, mean/SD by site, t-test.

Plots Histogram of the distribution of mean gene expression boxplot of tree circumference by site and year.
Statistic: Number of genes with a mean less than 10; change in mean with site, t-test p-value (e.g. p=0.06229 is no significant difference at alpha=0.05).


# Part2

Examining biological sequence diversity

purpose

This project comprises R script that will be utilized in the analysis and comparison of genomic and proteomic data of Bifidobacterium and E. coli. The scripts simplify the process of data acquisition, preprocessing, statistical analysis and visualization in order to reveal the variation in genome content, genes structure, codon usage, and sequence motifs. And the end result is to retrieve genomic sequences for Bifidobacterium and E. coli from the Ensembl database for downstream analysis.

Main step 

1 Data Retrieval & Parsing
Loads the CDS data of the two organisms off Ensembl.

2 Genome Overview
Computes the total amount of CDS, total coding base pairs and average length of sequence.

3 Base Composition
calculates the frequency of the nucleotides (A, T, G, C) of each organism.

4 Amino Acid Analysis
Converts DNA into protein sequences and matches the frequency of amino acids.

5 Codon Usage Bias
Calculates the relative synonymous codon usage (RSCU) and visualizes patterns of bias.

6 Protein k-mer Analysis
Determines most over and under-represented short peptide motifs (3-5 amino acids) in Bifidobacterium as compared to E. coli.

Inputs

ecoli_cds.fa – FASTA file of E. coli coding DNA sequences.

bifido_cds.fa – FASTA file of Bifidobacterium coding DNA sequences.

Outputs

Data frame: The results stored in k-mer data frames of each k.

Tables: Best over/under-represented k-mers by each organism, comparisons (e.g. ratios in human vs. E. coli, although the script can be adjusted to bifido).

Plots: Comparison between the obs/exp ratios of top k-mers in organisms.

Statistics: Ratio of observed/expected frequencies, log2 fold changes of frequencies.
