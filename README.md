## NGS-Analysis-in-R/Bioconducot

Sequence Analysis Tutorial in R and Bioconductor. 

### Introduction
Here I tried to learn how to Analyse NGS in R without using Linux Terminal.

## Why NGS Analysis with R/Bioconductor?

+ Hundreds of reusable NGS packages are available
+ Invent new things rather than reinventing existing ones
+ Many NGS methods require advanced statistical methods
+ Many NGS applications share similar analysis needs. Most of them have
existing solutions.
+ Access to advanced and reproducible genome graphics

## R Base
Some basic string handling utilities. Wide spectrum of numeric data analysis tools.

## Bioconductor
Bioconductor packages provide much more sophisticated string handling utilities for sequence analysis (Lawrence et al. 2013; Huber et al. 2015).

## Bioconductor Package Requirements

To install bioconductor packages, execute the following lines in the R console. Please also make sure that you have a recent R version installed on your system. R versions 3.3.x or higher are recommended.

source("https://bioconductor.org/biocLite.R")

if (!requireNamespace("BiocManager", quietly = TRUE))

install.packages("BiocManager")
BiocManager::install(c("Biostrings", "GenomicRanges", "rtracklayer", "systemPipeR", "seqLogo", "ShortRead"))





Last login: Tue Apr 29 09:59:51 on ttys000
(base) mhasan@MacBook-Pro ~ % ssh mehadi@gryffindor.nri.bcm.edu 
ssh: connect to host gryffindor.nri.bcm.edu port 22: Undefined error: 0
(base) mhasan@MacBook-Pro ~ % ssh mehadih@skyriver.nri.bcm.edu 
mehadih@skyriver.nri.bcm.edu's password: 
Welcome to Ubuntu 22.04.3 LTS (GNU/Linux 6.5.0-15-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

Expanded Security Maintenance for Applications is not enabled.

274 updates can be applied immediately.
165 of these updates are standard security updates.
To see these additional updates run: apt list --upgradable

18 additional security updates can be applied with ESM Apps.
Learn more about enabling ESM Apps service at https://ubuntu.com/esm


The list of available updates is more than a week old.
To check for new updates run: sudo apt update

Welcome to Bright Cluster Manager 9.2 
 
                                        Based on Ubuntu Jammy Jellyfish 22.04
                                                    Cluster Manager ID: #00000

Use the following commands to adjust your environment:                        
 
'module avail'            - show available modules                            
'module add <module>'     - adds a module to your environment for this session
'module initadd <module>' - configure module to be loaded at every login
                            (Note: initadd is available only for Tcl modules)
 
-------------------------------------------------------------------------------
Last login: Fri Apr 25 20:24:55 2025 from 10.70.15.96
(base) mehadih@leia1:~$ 
(base) mehadih@leia1:~$ cd
(base) mehadih@leia1:~$ ls
bioinformatics  miniconda3  my_cache_dir  todolist  work_bcm
(base) mehadih@leia1:~$ cd bioinformatics/
(base) mehadih@leia1:~/bioinformatics$ ls
collab  liuzlab  ngsalex  tools
(base) mehadih@leia1:~/bioinformatics$ cd ..
(base) mehadih@leia1:~$ cd  work_bcm/
(base) mehadih@leia1:~/work_bcm$ ls
mhasan_projects
(base) mehadih@leia1:~/work_bcm$ cd mhasan_projects/
(base) mehadih@leia1:~/work_bcm/mhasan_projects$ ls
dataset_2024  project2024  project2025  scripts_mhasan
(base) mehadih@leia1:~/work_bcm/mhasan_projects$ pwd
/home/mehadih/work_bcm/mhasan_projects
(base) mehadih@leia1:~/work_bcm/mhasan_projects$ 








(base) mehadih@leia1:~/work_bcm/mhasan_projects$ ls
dataset_2024  project2024  project2025  scripts_mhasan
(base) mehadih@leia1:~/work_bcm/mhasan_projects$ pwd
/home/mehadih/work_bcm/mhasan_projects
(base) mehadih@leia1:~/work_bcm/mhasan_projects$ cd
(base) mehadih@leia1:~$ pwd
/home/mehadih
(base) mehadih@leia1:~$ cd /home/mehadih/work_bcm/mhasan_projects
(base) mehadih@leia1:~/work_bcm/mhasan_projects$ mv scripts_mhasan/ /home/mehadih
(base) mehadih@leia1:~/work_bcm/mhasan_projects$ cd
(base) mehadih@leia1:~$ ls
bioinformatics  miniconda3  my_cache_dir  scripts_mhasan  todolist  work_bcm
(base) mehadih@leia1:~$ mv scripts_mhasan/ mehadi
(base) mehadih@leia1:~$ 









(base) mehadih@leia1:~$ ls
bioinformatics  mehadi  miniconda3  my_cache_dir  todolist  work_bcm
(base) mehadih@leia1:~$ cd mehadi/
(base) mehadih@leia1:~/mehadi$ ks
ks: command not found
(base) mehadih@leia1:~/mehadi$ ls
git_command          scripts-ncbi-geo         star_read_merge
motif_project        scripts_nextflow         star_scripts_hamin
scripts-go-kegg-ora  scripts_salmon           star_scripts_yanli
scripts_gsva         scripts_variant_calling  vim_command
(base) mehadih@leia1:~/mehadi$ 













(base) mehadih@leia1:~/mehadi$ cd scripts_gsva/
(base) mehadih@leia1:~/mehadi/scripts_gsva$ ls
data  plots  results  scripts
(base) mehadih@leia1:~/mehadi/scripts_gsva$ cd scripts/
(base) mehadih@leia1:~/mehadi/scripts_gsva/scripts$ ls
gsva_esme.Rmd  gsva_trial.Rmd  pathway-analysis_rnaseq_03_gsva.Rmd
(base) mehadih@leia1:~/mehadi/scripts_gsva/scripts$ vim gsva_esme.Rmd 

















coldata2F = xp_design |>
  filter((genotype == "WT" | genotype == "Atxn1L_KO")
         & (gender=="F"))

coldata2F$sampleID
```

# *comparison-3: WT-Cic_KO* Mutant vs WT
```{r}
# Male
coldata3M = xp_design |>
  filter((genotype == "WT" | genotype == "Cic_KO")
         & (gender=="M"))

coldata3M$sampleID


# Female
coldata3F = xp_design |>
  filter((genotype == "WT" | genotype == "Cic_KO")
         & (gender=="F"))

coldata3F$sampleID
                                                              174,1         25%



## Bioconductor packages use in NGS:

* Biostrings: general sequence analysis environment
* ShortRead: pipeline for short read data
* IRanges: low-level infrastructure for range data
* GenomicRanges: high-level infrastructure for range data
* GenomicFeatures: managing transcript centric annotations
* GenomicAlignments: handling short genomic alignments
* systemPipeR: NGS workflow and report generation environment
* Rsamtools: interface to samtools, bcftools and tabix
* BSgenome: genome annotation data
* biomaRt: interface to BioMart annotations
* rtracklayer: Annotation imports, interface to online genome browsers
* HelloRanges: Bedtools semantics in Bioc’s Ranges infrastructure

## Sequences in Bioconductor
XString for single sequence :

* DNAString: for DNA
* RNAString: for RNA
* AAString: for amino acid
* BString: for any string

XStringSet for many sequences:

* DNAStringSet: for DNA
* RNAStringSet: for RNA
* AAStringSet: for amino acid
* BStringSet: for any string

QualityScaleXStringSet for sequences with quality data:

* QualityScaledDNAStringSet: for DNA
* QualityScaledRNAStringSet: for RNA
* QualityScaledAAStringSet: for amino acid
* QualityScaledBStringSet: for any string

## Sequence Import and Export
Download the following sequences to your current working directory and then import them into R:

https://ftp.ncbi.nlm.nih.gov/genomes/archive/old_genbank/Bacteria/Halobacterium_sp_uid217/AE004437.ffn


# NGS Sequences
Sequence and Quality Data: FASTQ Format

Four lines per sequence:

ID
Sequence
ID
Base call qualities (Phred scores) as ASCII characters

The following gives an example of 3 Illumina reads in a FASTQ file. 

1. @SRR038845.3 HWI-EAS038:6:1:0:1938 length=36
2. CAACGAGTTCACACCTTGGCCGACAGGCCCGGGTAA
3. +SRR038845.3 HWI-EAS038:6:1:0:1938 length=36
4. BA@7>B=>:>>7@7@>>9=BAA?;>52;>:9=8.=A

## Sequence and Quality Data: QualityScaleXStringSet
Phred quality scores are integers from 0-50 that are stored as ASCII characters after adding 33. The basic R functions rawToChar and charToRaw can be used to interconvert among their representations.

## Range Operations
Important Data Objects for Range Operations.
* IRanges: stores range data only (IRanges library)
* GRanges: stores ranges and annotations (GenomicRanges library)
* GRangesList: list version of GRanges container (GenomicRanges library)
