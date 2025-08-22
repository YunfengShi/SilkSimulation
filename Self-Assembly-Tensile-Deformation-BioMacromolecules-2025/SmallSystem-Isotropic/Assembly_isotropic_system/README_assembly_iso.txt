This repository contains files and scripts for simulating the assembly of an isotropic (H8S24)16 silk system using LAMMPS.

<Required LAMMPS Version>
This simulation uses a customized GPU-enabled version of LAMMPS with a modified bump. Download the required version here:
https://github.com/mppotter/lammps.git

<Repository Contents>
s_hydro2: LAMMPS input script to simulate the system assembly for a small testing system.
log.lammps: Log file generated from the simulation.
resultingsilk.data: Final output data file containing the assembled structure.

<Simulation processes>
The simulation performs the following steps:
1. Read data: Loads s1.data, generated from a previous initialsetup simulation.
2. Hydrostatic Compression: Applies low pressure (P = 0.001 reduced unit) 
3. Dehydration : Gradually removes solvent particles from the system.
4. High-Pressure Compression: Further compresses the system at high pressure (P = 1 reduced unit).
5. Decompression
6. Relaxation

<Output files>
You can find the following files from a successful simulation run.
resultingsilk.data: Final data file representing the assembled silk structure.
log.lammps: Log file capturing details of the run.
lata4olivia_assembly: Dump file containing trajectories during the simulation.
