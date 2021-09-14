# stLearn: integrating spatial location, tissue morphology and gene expression to find cell types, cell-cell interactions and spatial trajectories within undissociated tissues
Duy Pham, Xiao Tan, ProfileJun Xu, Laura F. Grice, Pui Yeng Lam, Arti Raghubar, Jana Vukovic, Marc J. Ruitenberg, ProfileQuan Nguyen
The University of Queensland

Three data types:
- Spatial dimensionality,
- tissue morphology, and
- transcriptomics

1. Normalize genes: use morphological similarity + neighborhood smoothing; subcluster clustes by spatial separation
2. pseudo-space-time (PST(spatial distance, gene expression)); MST on PST -> spatial transition; model non-invasive -> invasive
3. cell-cell interaction hotspot: high ligand-receptor + diverse cell type 

## Background
- Spatial transcriptomics
- Current methods insufficient
- (SpaCell: integrating tissue morphology and spatial gene expression to predict disease cells)
