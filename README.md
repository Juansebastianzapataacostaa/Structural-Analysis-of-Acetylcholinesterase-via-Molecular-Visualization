# Structural-Analysis-of-Acetylcholinesterase-via-Molecular-Visualization
Structural bioinformatics analysis of Acetylcholinesterase (AChE) from Drosophila melanogaster using UCSF Chimera. The study compares two crystallographic structures — the native enzyme and an enzyme-inhibitor complex — to characterize active site geometry, ligand interactions, surface charge distribution, and conformational dynamics during catalysis.


Background

Acetylcholinesterase (AChE) is one of the most catalytically efficient enzymes in nature, responsible for hydrolyzing the neurotransmitter acetylcholine. Its mechanism involves covalent intermediate catalysis and acid-base catalysis driven by a precisely arranged catalytic triad at the active site.

This project analyzes two structures of AChE from Drosophila melanogaster deposited in the RCSB Protein Data Bank:

PDB IDDescriptionResolutionMethod1QO9Native AChE (no ligand)2.70 ÅX-ray crystallography1QONAChE + inhibitor I40 (tacrine derivative)2.72 ÅX-ray crystallography

Both structures share space group P 4₃ 2₁ 2.


Analysis overview

1. Crystallographic quality assessment (wwPDB validation)

Evaluated Rfree, Clashscore, Ramachandran outliers, sidechain outliers and RSRZ outliers for both structures using the wwPDB validation report. Both structures presented low percentile rankings across metrics, indicating limitations in model quality relative to structures of similar resolution.

2. Secondary structure characterization

Identified and compared β-sheet strands and α-helices across both structures using UCSF Chimera's secondary structure coloring:


1QO9: 11 β-strands
1QON: 12 β-strands
Longest α-helix (both structures): GLY 424.A → ARG 454.A (30 residues)
Second longest: ARG 499.A → GLY 520.A (21 residues)


3. Surface properties and charge distribution

Mapped hydrophobicity surface and Coulombic electrostatic surface to determine:


Polar/hydrophilic residues localize to the protein exterior
Apolar/hydrophobic residues concentrate in the protein interior, lining the active site cavity
Negative charges dominate the active site region, facilitating interaction with the positively charged acetylcholine substrate


4. Ligand-protein interactions (1QON — inhibitor I40)

Analyzed the tacrine derivative I40 (9-(3-iodobenzylamino)-1,2,3,4-tetrahydroacridine) bound in the active site gorge:


23 of 42 I40 atoms interact directly with hydrophobic protein residues
Active site residues identified: TRP 370, 162, 82, 71, 374 (aromatic); PHE 371, 330 (aromatic); HIS 480 (basic); LEU 479, ILE 484, GLY 481, 149, 150, 151 (apolar); GLU 237, 80 (acidic)
No hydrogen bonds between I40 and enzyme residues — consistent with predominantly hydrophobic active site
Two inter-residue H-bonds identified: TRP370–PHE371 (6.234 Å) and LEU479–HIS480 (5.237 Å)


5. Active site location

The active site is buried in a deep gorge within the protein core. Ligand access requires conformational rearrangement — consistent with the "breathing" motion of active site loops during catalysis.

6. Conformational dynamics

Morph Conformations analysis (MatchMaker + MD Movie) between 1QO9 and 1QON revealed:


Dominant motion in α-helices surrounding the active site gorge
β-sheets show restricted, localized movement
Active site loop flexibility facilitates substrate entry and product release



Tools & databases

Tool / ResourcePurposeUCSF ChimeraMolecular visualization and structural analysisRCSB Protein Data BankCrystallographic structure retrievalwwPDB Validation ServerStructure quality assessmentChimera — Coulombic Surface ColoringElectrostatic surface mappingChimera — FindHbondHydrogen bond identificationChimera — Clashes/ContactsVan der Waals contact analysisChimera — Morph ConformationsConformational dynamics visualization


Repository structure

FileDescriptionresults/Chimera visualization screenshots (ribbons, all-atoms, surface, active site)report/parcial_2.pdfFull analysis report with images and interpretationsREADME.mdProject overview


 Key findings


AChE has a predominantly hydrophobic active site gorge that accommodates the acylcholine moiety of substrates and inhibitors
The active site is negatively charged, consistent with attraction of the positively charged choline head group of acetylcholine
I40 binds through van der Waals and aromatic interactions (23/42 atoms in direct contact) with no hydrogen bonds to the enzyme
Conformational flexibility of α-helical loops at the gorge entrance enables substrate access and product release
Both structures showed moderate crystallographic quality with limitations in Clashscore and sidechain outlier metrics



Author

Juan Sebastián Zapata Acosta
Microbiologist — MSc Candidate in Computational Biology · Universidad de los Andes
GitHub · LinkedIn · Email


References


Harel, M.; Silman, I.; Sussman, J.L. (2021). Native AChE from Drosophila melanogaster. RCSB PDB. https://www.rcsb.org/structure/1QO9
Harel, M.; Silman, I.; Sussman, J.L. (2021). AChE from Drosophila melanogaster complex with tacrine derivative I40. RCSB PDB. https://www.rcsb.org/structure/1QON
Pettersen et al. (2004). UCSF Chimera — a visualization system for exploratory research and analysis. J Comput Chem, 25(13), 1605–12.



📄 License

MIT License — free to use with attribution.
