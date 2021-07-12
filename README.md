## NGS-Analysis-in-R
Sequence Analysis Tutorial in R and Bioconductor. 

### Introduction
Here I tried to learn how to Analyse NGS in R without using Linux Terminal.

## R Base
Some basic string handling utilities. Wide spectrum of numeric data analysis tools.

## Bioconductor
Bioconductor packages provide much more sophisticated string handling utilities for sequence analysis (Lawrence et al. 2013; Huber et al. 2015).

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
