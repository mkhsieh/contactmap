Contact analysis from MD trajectory (current only for dcd files)
Dependency: 
  numpy
  matplotlib.pyplot
  pyemma
  itertools
  mdtraj
  os, time, argparse

usage: contact.py [-h] [--pdb PDB] [--traj TRAJ [TRAJ ...]] [--sel1 SEL1 [SEL1 ...]] [--sel2 SEL2 [SEL2 ...]] [--cutoff CUTOFF] [--DistanceMap] [--ContactMap] [--outfolder OUTFOLDER]
