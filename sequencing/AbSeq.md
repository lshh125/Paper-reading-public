# Abseq: Ultrahigh-throughput single cell protein profiling with droplet microfluidic barcoding

Payam Shahi, Samuel C. Kim, John R. Haliburton, Zev J. Gartner & Adam R. Abate

UCSF



## Abstract

- Motivation: protein -- Primary effector
- Restriction: small amount
- Method: DNA-tagged antibody, cell barcoding



## Capacity

- 10,000 single cells
- 20M reads = 10k cells * 10 antibodies * 200 counts/(antibody * cell)^-1
- Even less (1/10) after removing PCR duplicates



## Bioinfo workflow

- Filtering sequencing error in cell barcode: 95% reads in large groups
- Filtering error in tag sequences: cells with >90% known tags
- Similar cell barcodes: Hamming distance
- UMI



## Notes

Jurkat vs Raji: CD3 vs CD19

Surface vs internally-expressed markers



