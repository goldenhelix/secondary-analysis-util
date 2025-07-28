# Secondary Analysis Utilities

This repository contains tasks that can be used in tandem with secondary and tertiary analysis tools. These tasks allow users to track secondary analysis results and quality metrics and ensure file formats are consistent for use with Sentieon and VarSeq. 

# Tasks

Below are the list of tasks and their usage. 

## Compress and Index Genomic Files

This task can be used to either compress and index genomic files, or check for correct compression and indexing formats. Supported file types are: 
- VCF
- BAM
- CRAM
- BED
- FASTQ
Additional options define whether to remove uncompressed files, index non-indexed files, search subdirectories, or search for a specific pattern (e.g., only perform selected actions for a specific sample in a directory).

## Update Quality Control Catalog

This task updates a given VSWarehouse 3 catalog with quality metrics from secondary and tertiary analysis steps. 
