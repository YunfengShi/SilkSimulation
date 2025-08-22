This repository contains files and scripts for generating the initial configuration of an anisotropic (H8S24)16 silk system using LAMMPS.

<Required LAMMPS Version>
This simulation uses a customized GPU-enabled version of LAMMPS with a modified bump. Download the required version here:
https://github.com/mppotter/lammps.git

<Repository Contents>
s2_ani: LAMMPS input script for building and preparing the initial silk configuration for a big system.
log.lammps: Log file from the simulation run.
before.data: Output data file before displacement.
after.data: Output data file after displacement.

<Simulation processes>
The simulation performs the following steps:
1. Chain Construction: Builds a single 16-unit silk chain.
2. Preparation of multi-chain system: Replicates the system to create 1152 chains.
3. Displacement of chains: Randomly displaces chains along the x-direction to break artificial periodicity.

<Output files>
before.data: data file immediately after chain replication (no displacement).
after.data: data file with the system configuration.
log.lammps: Log file detailing the simulation process.
