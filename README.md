# Investigation of the impact of P-adicity on the Genetic Code of the Coronavirus: Sequence Analysis and Clustering

This project explores the genetic structure of several coronaviruses and examines how P-adic distance can provide insights into the similarities and differences between surface proteins. Additionally, traditional Hamming and Edit distances are used for comparison, and hierarchical clustering is applied to group genetic sequences based on Edit distance.

## Introduction

Coronaviruses are a large family of viruses that can cause illness in animals and humans, including SARS, MERS, and COVID-19. Understanding the genetic structure of these viruses is crucial for the development of diagnostic tools, therapies, and vaccines.

This project focuses on the analysis of surface proteins (such as spike proteins) of several coronaviruses, including:
- SARS-CoV
- MERS-CoV
- Bovine coronavirus (BCoV)
- Human coronavirus 229E (HCoV-229E)
- Human coronavirus OC43 (HCoV-OC43)

We use P-adic distances, a unique mathematical approach, to analyze and compare genetic sequences.
## Dataset

All genetic sequences were retrieved from the [National Center for Biotechnology Information (NCBI)](https://www.ncbi.nlm.nih.gov/) database. The dataset includes the RNA sequences that code for proteins in the coronaviruses listed above.

## Preprocessing

The preprocessing steps include:
1. **Identifying Open Reading Frames (ORFs)**: ORFs are regions in the RNA sequence that potentially code proteins. This step allows us to extract meaningful portions of the genetic data for analysis.
2. **Translation**: The RNA sequences are translated into amino acid sequences based on the standard genetic code.
3. **Manual Correction**: For proteins that were not automatically identified, additional manual curation was performed to ensure accuracy.

## Analysis

The project uses various distance metrics to analyze the genetic sequences:
- *P-adic distance*: A mathematical tool used to analyze the genetic code based on p-adic numbers (with p = 5 and p = 2). It provides detailed insights into how codons (triplets of nucleotides) are related in terms of the genetic code.
- *Hamming distance*: Measures the differences between sequences of the same length by counting the positions where the sequences differ.
- *Edit distance*: Measures the number of operations (insertion, deletion, substitution) needed to convert one sequence into another.

The key surface proteins analyzed include spike proteins, which play a crucial role in the virus's ability to bind to and enter host cells.

## Clustering

After computing the distance matrices, hierarchical clustering is applied to group the genetic sequences based on their similarities:
- *Hierarchical Agglomerative Clustering*: This method builds a hierarchy of clusters by iteratively merging the closest clusters until only one cluster remains. The dendrogram generated from this clustering process helps visualize the relationships between the sequences.
- *Principal Component Analysis (PCA)*: Used to reduce the dimensionality of the data and visualize the clusters in a two-dimensional space.

## Results

The analysis reveals important insights into the relationships between the coronaviruses:
- *P-adic distance* shows detailed genetic differences, emphasizing the importance of certain nucleotide positions in codons.
- *Hamming distance* provides a more general view of genetic differences.
- *Edit distance* and hierarchical clustering reveal clusters of sequences that share common evolutionary or functional characteristics.

The analysis highlights similarities between certain coronavirus proteins, such as the spike proteins of Bovine coronavirus (BCoV) and Human coronavirus OC43 (HCoV-OC43), both of which use hemagglutinin-esterase (HE) proteins.

## How to Run

1. Clone the repository.
2. Install the required dependencies:
   ```bash
   pip install biopython scikit-learn numpy pandas matplotlib seaborn
3. Run scripts.
