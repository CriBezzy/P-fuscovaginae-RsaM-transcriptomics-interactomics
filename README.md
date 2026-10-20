# P-fuscovaginae-RsaM-transcriptomics-interactomics
Data supporting the characterization of RsaM-mediated regulation in Pseudomonas fuscovaginae, including RNA-seq differential expression, RsaM protein–protein pull-down mass spectrometry, and pfsI RNA–protein pull-down datasets.

This repository contains datasets generated to investigate quorum-sensing regulation and the role of RsaM in Pseudomonas fuscovaginae UPB0736. The repository includes whole-transcriptome differential gene expression data comparing the 0736IRIM mutant with the UPB0736 wild type, as well as mass-spectrometry datasets from protein–protein and RNA–protein pull-down experiments designed to identify potential RsaM-associated proteins and proteins interacting with pfsI mRNA.

- 0736IRIMvsUPB0736_deg


Complete results of differential gene expression analysis between P. fuscovaginae 0736IRIM and UPB0736 
following whole transcriptome sequencing. 

The analysis was performed by Novogene. 
The table provides full list of P. fuscovaginae genes (annotated by Novogene), with DESeq2-normalized counts for each gene in each biological
replicate, together with log2 fold change in expression (0736IRIM vs UPB0736) and unadjusted and adjusted p-values. 
The unnormalized read counts and FPKMs for each gene are also listed.


- protein-protein pull-down_diff_enr

The list of P. fuscovaginae proteins differentially enriched in pull-downs with His-tagged RsaM or untagged RsaM (controls) followed by mass spectrometry. 

His-tagged RsaM was expressed from the vector pLAH30RsaM (rsaM gene cloned into vector pLAH30), while untagged RsaM was expressed from the vector pBBRSAM
(rsaM gene cloned into vector pBBR1MCS-5). Both proteins were expressed in the strain P. fuscovaginae 0736IRIM. 
The mass spectrometry data were searched against protein sequences obtained from the NCBI Protein sequence database for Pseudomonas fuscovaginae UPB0736.
The analysis was performed in the FragPipe analyst using standard default parameters.Perseus-type imputation was used. 
Statistical significance was evaluated using an adjusted p-value threshold of 0.05 and followed by correction using Benjamini-Hochberg procedure.
The list of significantly enriched proteins is provided with log2 fold difference in occurence (0736IRIM (pLAH30RsaM) vs 0736IRIM (pBBRSAM)), together with unadjusted 
and adjusted p values. The table includes an imputation status indicator followed by a column listing the frequency of missing observations before the
imputation.

- RNA-protein pull-down_diff_enr

The list of P. fuscovaginae proteins that were present in all three biological replicates that used pfsI mRNA as bait
and were absent in all three bead-only controls. 

pfsI mRNA was synthesized via in vitro transcription. The protein extracts used in the pull-downs were obtained from P. fuscovaginae 0736IRIM (RsaM-expressing strain).
The mass spectrometry data were searched against protein sequences obtained from the UniProt Knowledgebase using the species-level taxonomic identifier (Taxon ID: 53407) 
for Pseudomonas asplenii (P. fuscovaginae is a later heterotypic synonym of P. asplenii).
Data analysis was subsequently performed in the FragPipe Analyst using the absence/presence feature. Statistical imputation was bypassed, and a filter 
requiring protein presence in all three biological replicates containing the RNA-bait, and absence in all three bead-only controls, was used to identify potential interactors 
with high confidence. 
The protein list is shown with the total number of detected unique peptides and corresponding MaxLFQ intensities. 
