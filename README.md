
📌 Overview

This project explores how machine learning can be applied to synthetic yeast strain engineering data.
It simulates a realistic DBTL (Design‑Build‑Test‑Learn) workflow using:

pandas for data generation and manipulation

scikit‑learn for preprocessing, PCA, and K‑means clustering

seaborn/matplotlib for visualization

multi‑omics features (transcriptomics, fluxomics, proteomics, metabolomics)

The goal is to demonstrate how computational tools can reveal biological structure in engineered strains.

🎯 Objectives
Generate a synthetic dataset of engineered S. cerevisiae strains

Add realistic multi‑omics features

Preprocess data using scaling + encoding

Apply PCA → K‑means to identify strain clusters

Visualize correlations and cluster separation

Interpret clusters in a strain‑engineering context

Save plots for GitHub documentation

🧪 Dataset Description
Phenotype Features
Product titer (g/L)

Growth rate (1/hr)

Stress tolerance score

Genotype Features
Edit count

Engineered pathway (Mevalonate / Shikimate / Glycolysis)

Omics Features
Gene expression (MevA transcript level)

Metabolic flux (MVA pathway)

Protein abundance (MevA)

Metabolite concentration

Enzyme activity score

These features mimic real multi‑omics datasets used in metabolic engineering.

🔧 Methods
1. Preprocessing
One‑hot encoding for pathway labels

Robust scaling to handle biological noise

PCA for dimensionality reduction

2. Clustering
K‑means (k = 3)

Cluster labels added back to the dataset

Cluster-wise mean values computed for interpretation

3. Visualization
PCA cluster plot

Omics correlation heatmap

Pairplot for multi‑omics relationships

Cluster summary table (saved as PNG)

📊 Key Results
Cluster 0 — High Producers
High titer

High protein abundance

High enzyme activity
Interpretation: Efficient producers; ideal candidates for scale-up.

Cluster 1 — Flux‑Driven but Bottlenecked
Moderate titer

High flux

Low protein
Interpretation: Pathway flux is high but enzyme levels are limiting.

Cluster 2 — Overexpressors
Lower titer

High gene expression

High protein

Moderate flux
Interpretation: Likely experiencing feedback inhibition or metabolic imbalance.
