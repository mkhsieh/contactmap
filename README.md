Contact information analysis for MD trajectory (current only for dcd files) from biomolecules systems.

Dependency: python 3, numpy, matplotlib.pyplot, pyemma, itertools, mdtraj, os, argparse

Usage: contact.py [-h] [--pdb PDB] [--traj TRAJ [TRAJ ...]] [--sel1 SEL1 [SEL1 ...]] [--sel2 SEL2 [SEL2 ...]] [--cutoff CUTOFF] [--DistanceMap] [--ContactMap] [--outfolder OUTFOLDER]
Note: 
1. trajectory files could be added as a list 
2. atomselection method as mdtraj https://mdtraj.org/1.9.4/atom_selection.html
3. cutoff unit in angstrom

For protein systems, user could just use alpha carbons for both selections, as following example:

python contact.py --pdb protein.pdb --traj dyn1.dcd dyn2.dcd dyn3.dcd --sel1 name CA --sel2 name CA --cutoff 9 --DistanceMap --ContactMap --outfolder outfolder

or select a range of residue:  
python contact.py --pdb protein.pdb --traj dyn1.dcd dyn2.dcd dyn3.dcd --sel1 residue 40 to 70 and name CA --sel2 reidue 80 to 120 and name CA --cutoff 9 --DistanceMap --ContactMap --outfolder outfolder

The contact distance map (DistanceMap.png) and contact frequency map (ContactMap.png) will be generated in the OUTFOLDER, the data will be storied as contact_dis.npy and contact_freq.npy files as well.
