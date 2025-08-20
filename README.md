# Secondary Analysis Utilities

This repository contains utility tasks that can be used in tandem with secondary and tertiary analysis tools. These tasks help ensure file formats are consistent for use with Sentieon and VarSeq, and provide essential file management capabilities for genomic data processing workflows.

## Tasks

### 🗜️ Compress and Index Genomic Files

**Purpose**: Compress, index, and validate genomic files to ensure compatibility with downstream analysis tools.

**Supported File Types**:
- **VCF** - Variant Call Format files
- **BAM** - Binary Alignment/Map files  
- **CRAM** - Compressed Reference-oriented Alignment/Map files
- **BED** - Browser Extensible Data files
- **FASTQ** - Sequence data files

**Key Features**:
- **File Conversion**: Convert between BAM and CRAM formats
- **Compression Control**: Selective compression for different file types
- **Indexing**: Automatic index file generation for supported formats
- **Cleanup Options**: Remove uncompressed files after processing
- **Pattern Matching**: Process specific files using search patterns
- **Recursive Processing**: Search subdirectories for genomic files
- **Error Handling**: Skip out-of-order VCFs with configurable behavior

**Use Cases**: Standardize file formats for Sentieon pipelines, prepare data for VarSeq analysis, optimize storage and access patterns.

---

### 📊 Create Coverage TSF

**Purpose**: Generate Coverage TSF files for optimal visualization in GenomeBrowse.

**Supported Input Formats**:
- **BAM** files with `.bai` index
- **CRAM** files with `.crai` index  
- **VCF** files with `.tbi` index

**Key Features**:
- **Pre-computation**: Generates zoomed-out viewing data for large genomic files
- **Batch Processing**: Handles multiple files in a single run
- **Recursive Search**: Option to process files in subdirectories
- **Error Resilience**: Continue processing on individual file failures
- **Reference Integration**: Uses workspace reference genome for calculations

**Note**: This task is redundant if using VSPipeline for VarSeq project creation, as coverage TSF files are generated automatically.

**Use Cases**: Prepare data for GenomeBrowse visualization, optimize performance for large genomic datasets, batch process multiple samples.

---

### 📦 Unarchive Files

**Purpose**: Extract compressed and archived files to prepare data for downstream analysis.

**Supported Archive Formats**:
- **ZIP** archives (`.zip`)
- **TAR** archives (`.tar`) 
- **Compressed TAR** archives (`.tar.gz`)

**Key Features**:
- **Multi-format Support**: Handles common compression formats
- **Batch Processing**: Processes all archives in a directory
- **Preserved Structure**: Maintains original directory organization
- **Automatic Detection**: Finds archives by file extension

**Use Cases**: Extract downloaded genomic datasets, prepare raw data for analysis pipelines, decompress reference files and annotations.

---

## System Requirements

All tasks require:
- **CPU**: 4 cores minimum
- **Memory**: 8 GB RAM minimum
- **Docker**: Containerized execution environment

## Getting Started

1. **Select a Task**: Choose the appropriate utility based on your data processing needs
2. **Configure Parameters**: Set input directories and processing options
3. **Execute**: Run the task with your genomic data
4. **Verify Output**: Check that files are properly processed and indexed

## Integration

These utilities are designed to work seamlessly with:
- **Sentieon** analysis pipelines
- **VarSeq** variant analysis workflows  
- **GenomeBrowse** visualization tools
- **VSPipeline** automated project creation

For questions or support, please refer to the individual task documentation or contact your system administrator. 
