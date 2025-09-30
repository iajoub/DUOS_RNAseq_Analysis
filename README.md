# Joubert et al., 2025 – Dual RNA-seq Analysis

Analysis scripts and processed data for **Joubert et al., 2025 (manuscript under review)**.  
This repository contains R Markdown scripts, metadata, and derived count matrices used for dual RNA-seq analysis of host–pathogen interactions in preterm, term, and adult whole-blood models challenged with *Staphylococcus epidermidis* and *Staphylococcus aureus*.

---

## Repository Structure

```text
.
├── Code/
│   ├── DerivedCountMatrix/
│   │   ├── count_matrix_filt.csv      # Host filtered count matrix (after QC filtering)
│   │   ├── count_matrix_SA.csv        # S. aureus count matrix
│   │   └── count_matrix_SE.csv        # S. epidermidis count matrix
│   │
│   ├── MetadataFiles/
│   │   ├── Human_Sample_MetaData.csv  # Metadata for human host samples
│   │   ├── SA_MetaData.csv            # Metadata for bacterial S. aureus samples
│   │   └── SE_MetaData.csv            # Metadata for bacterial S. epidermidis samples
│   │
│   ├── RawCountFiles/                 # Full raw count matrices (host + bacterial)
│   │   ├── host_counts_raw.csv
│   │   ├── SA_counts_raw.csv
│   │   └── SE_counts_raw.csv
│   │
│   └── Scripts/
│       └── Joubert2025_DUOS_DataAnalysis.Rmd  # Main R Markdown script reproducing host + bacterial analyses
│
├── LICENSE
└── README.md

---

## Software and Package Versions

### Read Processing and Mapping
- FastQC v0.12.1  
- MultiQC v1.18  
- Trimmomatic v0.39  
- RiboDetector v0.2.8  
- RNA-STAR v2.7.1a  
- Subread v2.0.6  

Reference Genomes  
- Staphylococcus epidermidis 1457 (CP020463, CP020462)  
- Staphylococcus aureus 29523 (CP009361, CP009362)  
- Human genome reference hg38  

### R Environment
- R v4.3.1  
- RStudio 2023.06.1+524  

### R Packages
- DESeq2 v1.40.2  
- WGCNA v1.72-1  
- impute v1.74-1  
- limma v3.56.2  
- STRINGdb (via STRING v12.0 API)  
- clusterProfiler v4.8.3  
- UpSetR v1.4.0  
- ggplot2 v3.4.4  
- pheatmap v1.0.12  
- ComplexHeatmap v2.16.0  
- VennDiagram v1.7.3  
- enrichplot v1.20.3  
- tidyverse v2.0.0  
- reshape2 v1.4.4  
- dplyr v1.1.4  
- gridExtra v2.3  
- org.Hs.eg.db v3.17.0  
- vegan v2.6.4  
- stats v4.3.1  

---

## Data Availability
- Raw sequencing reads: Can be accessed at https://www.ebi.ac.uk/biostudies/arrayexpress/studies/E-MTAB-14798.
- Processed data: All count matrices and metadata required to reproduce analyses are included in this repository.  

---

## Notes
- Outlier detection workflow and PCA plots before/after filtering are described in the manuscript (see Supplementary Fig. 6).  
- Both bacterial and host analyses are contained within the single R Markdown script.  

---

## License
- The analysis scripts in this repository are released under the [MIT License](LICENSE).  
- Derived count matrices and metadata files are released under the [Creative Commons Attribution 4.0 International (CC BY 4.0) license](https://creativecommons.org/licenses/by/4.0/).  

---

## Citation
If you use this repository, please cite: Joubert et al., 2025., Characterising Commensal and Pathogenic Staphylococcal Interactions with Neonatal and Adult Blood, . Scientific Reports. DOI: [forthcoming].
