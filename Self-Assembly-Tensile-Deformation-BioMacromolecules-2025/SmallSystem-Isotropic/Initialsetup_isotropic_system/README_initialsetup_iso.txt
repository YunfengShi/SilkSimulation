This repository contains files and scripts for generating the initial configuration of an isotropic (H8S24)16 silk system using LAMMPS.

<Required LAMMPS Version>
This simulation uses a customized GPU-enabled version of LAMMPS with a modified bump. Download the required version here:
https://github.com/mppotter/lammps.git

<Repository Contents>
s2 : LAMMPS input script for building and preparing the initial silk configuration for a small testing system.
log.lammps : Log file from a successful simulation run.
s1.data : Output data file from a successful simulation run.

<Simulation processes>
The simulation performs the following steps:
1. Chain Construction: Builds a single 16-unit silk chain.
2. Preparation of multi-chain system: Replicates the system to create 32 chains.
3. High-Temperature Relaxation.
4. Density reduction.
5. Cooling to room temperature.

<Output files>
You can find the following files from a successful simulation run.
s1.data: Final data file with the system configuration.
log.lammps : Log file capturing details of the run.
lata4olivia_initial : Dump file containing trajectory data during simulation.

