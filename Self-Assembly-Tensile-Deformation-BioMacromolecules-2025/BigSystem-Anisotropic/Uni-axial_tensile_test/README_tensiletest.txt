This repository contains files and scripts to simulate a uniaxial tensile test along the x-direction on the assembled silk system using LAMMPS.

<Required LAMMPS Version>
This simulation uses a customized GPU-enabled version of LAMMPS with a modified bump. Download the required version here:
https://github.com/mppotter/lammps.git

<Repository Contents>
s_tension2: LAMMPS input script for running the tensile test for the small testing system.
log.lammps: Log file for the relaxation stage before tensile loading.
log.tensile1: Log file for the tensile deformation stage.

<Simulation processes>
The simulation performs the following steps:
1. Read data : Loads resultingsilk.data, generated from a previous assembly simulation.
2. Relaxation before tensile loading.
3. Uni-axial tensile loading : Applies strain along the x-direction to simulate tensile loading.

<Output files>
You can find the following files from a successful simulation run.
log.lammps: Log file capturing details of the run during the relaxation stage.
log.tensile1: Log file capturing details of the run during the tensile test.
lata4olivia_tensile1: Dump file containing trajectories during tensile test.
