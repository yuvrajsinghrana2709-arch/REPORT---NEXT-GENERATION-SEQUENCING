# REPORT---NEXT-GENERATION-SEQUENCING
REPORT ON 10 DAYS NGS WORKSHOP.
Author: Yuvraj Rana

# What Is NGS 

Next-Generation Sequencing (NGS) is a high-throughput, massively parallel sequencing technology that allows for the simultaneous sequencing of millions of DNA fragments. It determines the precise order of nucleotide( A, T,C, G)much faster and cheaper than traditional Sanger sequencing

All the work was done using Galaxy an open source, web-based platform for data intensive biomedical research.For Data Download we used https://zenodo.org/records/4249555 We used Raw mouse mammary RNA-Seq data (fastq), uploaded the 4 files on galaxy and used certain tools-

<img width="1415" height="293" alt="Screenshot 2026-01-22 213537" src="https://github.com/user-attachments/assets/9db67498-114f-4103-9a84-32da2f3e58ed" />

# 1.Fastqc Tool

Think of FastQC as the "Report Card" for your sequencing run. Before you do any actual analysis (like finding mutations or assembling a genome), you must run this tool to see if your data is "clean" or "garbage."

<img width="1476" height="819" alt="Screenshot 2026-01-22 213917" src="https://github.com/user-attachments/assets/291a591d-13de-4d67-b7ca-9406b0392a5e" />

# 2. Trim Galore

Trim Galore is a Perl-based wrapper script used in bioinformatics to automate the quality control and trimming of High-Throughput Sequencing (NGS) data. It integrates the functionality of Cutadapt (for removing adapters and low-quality bases) and FastQC (for post-trimming quality checks) into a single, streamlined workflow.

<img width="1469" height="782" alt="Screenshot 2026-01-22 214408" src="https://github.com/user-attachments/assets/0ce8ba4c-bc48-47b9-9bdb-b9be23137924" />

# 3. Bowtie2

After you have cleaned your data with Trim Galore, you have millions of short DNA fragments (reads). Now, you need to figure out where exactly in the genome each fragment came from. Bowtie2 does this job.

<img width="1475" height="817" alt="Screenshot 2026-01-22 214701" src="https://github.com/user-attachments/assets/4a3009b5-5b67-4e85-b36e-85ba57340997" />

# 4. Featurecounts

FeatureCounts is the tool you use for Quantification (Counting). You have already aligned your reads to the genome using Bowtie2, but knowing where the reads are isn't enough. You need to know how many reads landed on Gene A versus Gene B. This tells you if a gene is highly expressed (active) or not

<img width="1469" height="813" alt="Screenshot 2026-01-22 214935" src="https://github.com/user-attachments/assets/6acc6f6c-4af3-4604-9ee6-b0dd668c22dc" />

# 5. DEseq2

DESeq2 is the final and most critical step in your RNA-Seq pipeline. It is the tool that performs Differential Gene Expression (DGE) analysis.

<img width="1475" height="811" alt="Screenshot 2026-01-22 215345" src="https://github.com/user-attachments/assets/dd92d419-8533-476d-881a-d4eda0bcc174" />

<img width="1467" height="821" alt="Screenshot 2026-01-22 215545" src="https://github.com/user-attachments/assets/65678690-a418-49ab-a65b-6d46d6c30e5a" />

<img width="1472" height="814" alt="Screenshot 2026-01-22 215701" src="https://github.com/user-attachments/assets/78562620-3b52-4768-808c-ca4c9cbc349e" />

<img width="1471" height="824" alt="Screenshot 2026-01-22 215801" src="https://github.com/user-attachments/assets/3f44cae3-f28d-47ff-8d45-5405a6dec8c8" />

# 6. Heatmap2

heatmap.2 is the specific R function (from the package gplots) used to create the most colorful and informative graph in your RNA-Seq project: the Heatmap.

<img width="1469" height="822" alt="Screenshot 2026-01-22 220024" src="https://github.com/user-attachments/assets/19b1dd99-0c3b-4867-b607-a8aeb8ffb5fd" />

# 7.KYOTO ENCYCLOPEDIA OF GENES AND GENOME (KEGG)

KEGG stands for the Kyoto Encyclopedia of Genes and Genomes. After you finish your DESeq2 analysis and Heatmap, you have a list of important genes. But a list of names (e.g., "PFK1, HK2, LDHA") is boring and hard to understand. KEGG is the tool that puts those genes onto a "Map" to show you how they work together

<img width="1218" height="861" alt="mmu04141_20260115_204416" src="https://github.com/user-attachments/assets/5aebe447-c049-49d3-821d-74aa2dddcf18" />


















