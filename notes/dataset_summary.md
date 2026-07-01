# GSE5281 — Dataset Notes

## Overview
GSE5281 is a gene expression dataset from post-mortem human brain tissue. It compares Alzheimer’s disease samples with healthy (non-demented) controls to identify differences in gene activity.

---

## Data type
Microarray gene expression data.

It measures gene expression levels (not DNA mutations or sequence changes). Each sample is a single brain tissue specimen from one individual.

---

## Groups
- Alzheimer’s disease patients  
- Non-demented controls  

Since the data is post-mortem, it’s a single timepoint snapshot. There is no disease progression captured.

---

## Brain regions
Includes multiple regions:
- hippocampus  
- entorhinal cortex  
- frontal cortex  
- additional cortical regions  

Hippocampus is likely the most important due to its role in memory, but all regions should be analyzed separately since effects may vary across them.

---

## Goal
Main goal is to identify gene expression differences associated with Alzheimer’s disease.

Expected outcomes:
- differentially expressed genes (up/down regulated)
- disrupted biological pathways
- signals related to memory and cognition

---

## Current interpretation
Treating this as a basic comparison:

Alzheimer’s vs controls → differential expression → identify consistent gene changes

Not fully sure yet which brain region will show the strongest signal. Hippocampus is usually the main focus in literature.

Some noise is expected due to post-mortem tissue variability.

---
## Next Steps

1. Run a first differential expression analysis in GEO2R
   - Group Alzheimer’s samples vs control samples (all brain regions combined first)
   - Check that groups are correctly assigned before running

2. Generate initial results
   - Identify top upregulated and downregulated genes
   - Sort results by p-value and fold change

3. Export results
   - Download full GEO2R output table (CSV)
   - Save into /results folder

4. Do a first quick scan of results
   - Look for obvious strong genes (very low p-values, high fold change)
   - Note any unexpected patterns

5. Only after this:
   - Decide whether to run region-specific analysis (HIP vs EC etc.)
   - Start pathway analysis (Enrichr / STRING)
