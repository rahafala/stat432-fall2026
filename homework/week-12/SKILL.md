---
name: clustering-report
description: Compare clustering algorithms on an unlabeled dataset, select one, and write a one-page report.  
disable-model-invocation: true
---

# Clustering Analysis Report
Run only when the user invokes this skill. The user supplies: dataset path,
feature columns, ID column, optional label column (for interpretation only),
seed, output folder. Ask if any are missing. Never assume dataset-specific facts; base every statement on computed results.

## Tools
Python (pandas, numpy, scikit-learn, matplotlib). One script must reproduce every number, figure, and table.

## Analysis rules
1. **Load and check.** Report n, p, missing values. Fit and select using
   features only; never use labels until the final interpretation step.
2. **Preprocessing.** standardize features unless it is already standardized. When p >> n, consider variance filtering and/or PCA. Justify the choice.
3. **Candidate algorithms.** At least three different clustering algorithms (PCA/UMAP alone does not count). K-means, hierarchical (linkage: average; distance: Euclidean), spectral (k-nearest-neighbors).
4. **Tuning and number of clusters.** Try K = 2..min(10, n/5) and spectral n_neighbors in {5, 10, 15}; choose K and n_neighbors by mean silhouette.
5. **Compare and select.** Select the highest mean silhouette; break ties with stability (ARI across 20 seeds), then the smaller K. Reject solutions with any cluster smaller than 5% of n.
6. **Interpret.** Only for the selected method: cluster sizes, what separates
   the clusters, and (if labels exist) a cross-tab of clusters vs labels.

## Report
Limit the report to **one printed page**, including all text, figures,
and tables. Show clustering results from **only one selected method**;
other methods may be named briefly to justify the choice, with no
results shown for them. format: Quarto `.qmd` -> PDF; letter size,
11pt, 0.75 in margins; hide code. Render and confirm one page; if too long,
cut text first. Sections, in order:
1. **Title** + one line: n, p, preprocessing, seed.
2. **Methods** (2-4 sentences): candidates, tuning, selection criteria.
3. **Selection evidence** small table (method, K,
   criterion score). Bold the selected method.
4. **Figure** (selected method only, readable). PC1 vs PC2
   colored by cluster (label as marker shape).
5. **Interpretation** (2-3 sentences): what the groups are; cross-tab vs labels.
6. **Limitations** (2-4 bullets). small n, sensitivity to
   preprocessing/K, labels used only after selection.
