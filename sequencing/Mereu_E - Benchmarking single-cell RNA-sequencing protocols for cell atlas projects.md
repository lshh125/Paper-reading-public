# Benchmarking single-cell RNA-sequencing protocols for cell atlas projects
Elisabetta Mereu et al.

- RNA capture efficiency, bias, scale and costs
- relative advantages for different applications


Protocol differences:
- library complexity （RNA molecules -> sequencing libraries)
- ability to detect cell-type markers
- predictive value (power to describe cell types/states)


Reference sample
- Human peripheral blood **60%**
  - cells in transition states
  - wide range of cell sizes, RNA content
- Mouse colon **30%**
1. a high degree of cell-type heterogeneity with various frequencies
2. closely related subpopulations with subtle differences in gene expression
3. a defined cell composition with trackable markers and 
4. cells from different species
- spike-in cell lines (HEK293T human **6%**, NIH3T3 mouse **3%**, MDCK dog **1%**)
  - assess batch effects
  - monitor cell-type composition

Benchmarking:
Cells: ~3,000 per protocol (>50,000 for reference)


Expectation for sequencing methods:
1. accurate, free of technical biases
2. applicable across distinct cell properties
3. fully disclose tissue heterogeneity (cell states) 
4. reproducible expression profiles
5. comprehensively detect population markers
6. integratable with other methods 
7. have predictive value with cells mapping confidently to a reference atlas


Observations:
- Higher fraction of mouse colon cells in unsorted and snRNA-seq data -> damaging during sample preparation -> no viability selection? More cells removed in filtering, higher cost
- Chromium v.3 better than v.2
- high technical reproducibility within the methods
- snRNA-seq more introns; scRNA-seq also high proportion of intronic/intergenic mapping
- snRNA: less genes detected than scRNA
- snRNA: UMAP similar to scRNA, correlation not so much
- Marker gene overlap is low among methods and between scRNA and snRNA;
- When more cells are included, snRNA and scRNA are similar interms of transcriptome complexity
