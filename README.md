# Expanded Benchmark

T cell receptors (TCRs) play a crucial role in the adaptive immune system. They are responsible for recognising antigenic peptides presented at the surface of infected cells by major histocompatibility complex (MHC) molecules, and triggering downstream immune responses to fight off disease.

This repository contains structural data of TCRs and pMHC complexes crystallised in bound and unbound form, serving as a set of benchmark test cases for computational docking tools. This dataset contains the 30 TCR-pMHC docking cases present in the [original TCR benchmark](https://tcr3d.ibbr.umd.edu/unbbou), as well as 14 new cases identified in the [STCRDab](http://opig.stats.ox.ac.uk/webapps/stcrdab/) and [Protein Databank](https://www.rcsb.org/) databases. This data was curated for work described in [Peacock and Chain (2021)](https://doi.org/10.3389/fimmu.2021.686127). 

Structures in the `raw` folder contain structural data as stored in the [Protein Databank](https://www.rcsb.org/). Original names for these PDB structures can be found in the table below.

Structures in the `imgt` folder have been preprocessed. Solvent and heteroatoms have been removed, as have disordered atoms. Residues with non-standard names in PDB format have been updated to their standard equivalents. Raw data that contained multiple co-crystalised protein structures has been reduced such that only one appears in each PDB file. Structures with missing atoms or residues at the binding interface were repaired using [Modeller](https://salilab.org/modeller/) using a protocol described in the [Modeller-Repair](https://github.com/innate2adaptive/Modeller-Repair) repository. TCRs in both the unbound and bound files have been re-numbered according to the IMGT numbering scheme. TCR chains have been relabelled with the IDs `D` and `E`, MHC chains with IDs `A` and `B`, and peptide chains with ID `C`. The position and orientation of each structure has been randomised.

Each docking case is named after the PDB code of the raw bound TCR-pMHC structure. Bound TCR-pMHC structures contain the suffix `_b.pdb`, unbound TCRs contain the suffix `_r_u.pdb` (where `r` stands for "receptor", and `u` stands for "unbound") and  unbound pMHCs contain the suffix `_l_u.pdb` (where `l` stands for "ligand", and `u` stands for "unbound"). Corresponding codes for the unbound TCR and unbound pMHC structures can be found in the table below. 

| Bound Complex | Unbound TCR | Unbound pMHC | MHC Class | IRMSD | F<sub>non-nat</sub> | Difficulty | 
| ------------- | ----------- | ------------ | --------- | ----- | ------------------- | ---------- |
|1AO7  <sup>*</sup> | 3QH3 | 1DUZ | I | 1.25 | 0.33 | rigid |
|1MI5  <sup>*</sup> | 1KGC | 1M05 | I | 1.25 | 0.48 | medium |
|1MWA  <sup>*</sup> | 1TCR | 1LEK | I | 1.14 | 0.3 | rigid |
|1OGA  <sup>*</sup> | 2VLM | 2VLL | I | 1.36 | 0.43 | medium |
|2BNR  <sup>*</sup> | 2BNU | 1S9W | I | 0.72 | 0.23 | rigid |
|2CKB  <sup>*</sup> <sup>‡</sup> | 1TCR | 1LEG | I | 1.17 | 0.45 | medium |
|2IAM  <sup>*</sup> | 2IAL | 1KLG | II | 0.87 | 0.24 | rigid |
|2IAN  <sup>*</sup> | 2IAL | 1KLU | II | 0.82 | 0.3 | rigid |
|2NX5  <sup>*</sup> <sup>†</sup> | 2NW2 | 1ZSD | I | 1.16 | 0.38 | rigid |
|2OI9  <sup>*</sup> | 1TCR | 3ERY | I | 1.1 | 0.41 | medium |
|2PXY  <sup>*</sup> | 2Z35 | 1K2D | II | 1.18 | 0.55 | medium |
|2PYE  <sup>*</sup> | 2PYF | 1S9W | I | 0.88 | 0.3 | rigid |
|3DXA  <sup>*</sup> <sup>†</sup> | 3DX9 | 3DX8 | I | 1.48 | 0.39 | rigid |
|3H9S  <sup>*</sup> | 3QH3 | 3H7B | I | 1.31 | 0.42 | medium |
|3KPR  <sup>*</sup> | 1KGC | 3KPQ | I | 1.37 | 0.55 | medium |
|3KPS  <sup>*</sup> | 1KGC | 3KPP | I | 1.31 | 0.48 | medium |
|3PWP  <sup>*</sup> | 3QH3 | 3PWL | I | 1.24 | 0.36 | rigid |
|3QDG  <sup>*</sup> <sup>†</sup> <sup>‡</sup> | 3QEU | 1JF1 | I | 0.91 | 0.31 | rigid |
|3QDJ  <sup>*</sup> <sup>‡</sup> | 3QEU | 2GUO | I | 0.94 | 0.28 | rigid |
|3SJV  <sup>*</sup> <sup>‡</sup> | 3SKN | 1M05 | I | 0.96 | 0.41 | medium |
|3UTT  <sup>*</sup> | 3UTP | 3UTQ | I | 0.75 | 0.4 | rigid |
|3VXR  | 3VXQ | 3VXN | I | 0.82 | 0.38 | rigid |
|3VXS  <sup>*</sup> <sup>†</sup> | 3VXQ | 3VXP | I | 0.89 | 0.35 | rigid |
|3W0W  <sup>*</sup> <sup>†</sup> <sup>‡</sup> | 3VXT | 3VXO | I | 0.94 | 0.42 | medium |
|4JFD  <sup>*</sup> <sup>†</sup> | 4JFH | 4JFP | I | 1.51 | 0.51 | medium |
|4JFF  | 4JFH | 1JF1 | I | 1.54 | 0.52 | medium |
|5C07  | 3UTP | 5C0E | I | 0.57 | 0.15 | rigid |
|5C08  | 3UTP | 5C0F | I | 0.65 | 0.43 | medium |
|5C09  | 3UTP | 5C0G | I | 0.59 | 0.24 | rigid |
|5C0A  | 3UTP | 5N1Y | I | 0.5 | 0.3 | rigid |
|5C0B  | 3UTP | 5C0I | I | 0.59 | 0.25 | rigid |
|5C0C  | 3UTP | 5C0J | I | 0.64 | 0.35 | rigid |
|5HHM  | 2VLM | 5HHN | I | 1.42 | 0.51 | medium |
|5HYJ  | 3UTP | 5C0D | I | 0.55 | 0.34 | rigid |
|5IVX  | 5IW1 | 3ECB | I | 1.29 | 0.38 | rigid |
|5NME  | 5NMD | 2V2W | I | 1.07 | 0.34 | rigid |
|5NMF  <sup>*</sup> <sup>†</sup> | 5NMD | 5NMH | I | 1.05 | 0.38 | rigid |
|5NMG  <sup>*</sup> <sup>†</sup> <sup>‡</sup> | 5NMD | 5NMK | I | 1.07 | 0.42 | medium |
|6AMU  | 3QEU | 6AMT | I | 1.16 | 0.41 | medium |
|6AVF  <sup>*</sup> <sup>†</sup> | 6AT6 | 6AT5 | I | 1.95 | 0.72 | medium |
|6CQL  <sup>*</sup> <sup>†</sup> | 6CPH | 6CPN | II | 0.78 | 0.23 | rigid |
|6CQQ  <sup>*</sup> <sup>†</sup> | 6CPH | 6CPO | II | 0.83 | 0.21 | rigid |
|6CQR  <sup>*</sup> <sup>†</sup> | 6CPH | 6CQJ | II | 0.85 | 0.26 | rigid |
|6EQB  | 4JFH | 2GUO | I | 1.62 | 0.55 | medium |

<sup>*</sup> TCR docking cases that feature in the TCR3d database <br>
<sup>†</sup> Cases that differ in I-RSMD score to those in the TCR3d database <br>
<sup>‡</sup> Cases that differ in docking difficulty category in the TCR3d database <br>

### Notes:
* A structure for 2NX5_r_u with improved modelling of the missing atoms and residues in one of its CDR3 loops has been uploaded to the `imgt` folder, since the publication of [Peacock and Chain (2021)](https://doi.org/10.3389/fimmu.2021.686127). Minor differences in the IRMSD and F<sub>non-nat</sub> values have been updated accordingly in the table above.
