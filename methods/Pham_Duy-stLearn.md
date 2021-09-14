# stLearn: integrating spatial location, tissue morphology and gene expression to find cell types, cell-cell interactions and spatial trajectories within undissociated tissues
Duy Pham, Xiao Tan, ProfileJun Xu, Laura F. Grice, Pui Yeng Lam, Arti Raghubar, Jana Vukovic, Marc J. Ruitenberg, ProfileQuan Nguyen
The University of Queensland

https://www.biorxiv.org/content/10.1101/2020.05.31.125658v1
https://stlearn.readthedocs.io/en/latest/

Three data types:
- Spatial dimensionality,
- tissue morphology, and
- transcriptomics

1. Normalize genes: use morphological similarity + neighborhood smoothing; subcluster clustes by spatial separation
2. pseudo-space-time (PST(spatial distance, gene expression)); MST on PST -> spatial transition; model non-invasive -> invasive
3. cell-cell interaction hotspot: high ligand-receptor + diverse cell type 

Cell types, trajectories, cell-cell interactions

## Background
- Spatial transcriptomics
- Current methods insufficient
- Need multimodal methods (SpaCell: integrating tissue morphology and spatial gene expression to predict disease cells)


## Methods
1. SME normalization: smoothing spots with similar mophology
2. SMEclust: Louvain + subcluster based on spatial info
3. Trajectory: 
    - PAGA on whole tissue
    - diffusion pseudotime
    - add spatial info
    - directed minimum spanning tree 
   **case study breast DCIS IDC**
    - Tree instead of a linear trajectory
    - Different sets of markers for clades
4. Interactions
    - L-R co-expression (CellphoneDB, etc.)
    - cell type diversity
   **case study breast DCIS IDC**
    - 7 CCI clusters
    - cluster 5: most interactions; immune cells
5. Microenvironment
    - factor analysis: PCA, ICA, FA
