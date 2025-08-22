This repository contains sub-repositories for simulating an isotropic (H8S24)16 silk system and an anisotropic (H8S24)16 silk system using Lammps (Please check Figure 1 and Supporting information file for more details)

The paper link is: https://doi.org/10.1021/acs.biomac.4c01623

[Particle Type]
	The silk system consists of eight particle types, each representing a different component (Please check Figure 1 and Supporting information file for more details)
-	Type 1: Ca
-	Type 2: Cb
-	Type 3: H
-	Type 4: B
-	Type 5: W
-	Type 6: P
-	Type 7: Sa
-	Type 8: Sb
-	Type 9: Not part of the silk structure, yet being used as a temporary placeholder type

[Silk Structure]

	The structure of each chain unit is determined by defining the region size in the x-direction of hard segment and soft segment.
	For hard segment, region "middle" for block is defined. For soft segment on the left, region "middle5" is defined. For soft segment on the right, region "middle2" is defined. 
	Different unit structures can be created by adjusting xlo and xhi of the region. In our customized lattice setup, two particles are filled in each unit box.

	Unit Structure  |  middle 5 |   |   middle  |   |  middle 2 |
					| xlo | xhi |   | xlo | xhi |   | xlo | xhi |
	------------------------------------------------------------------
	(H4S28)         |  0  |  7  |   |  7  |  9  |   |  9  |  16 |
	(H8S24)         |  0  |  6  |   |  6  |  10 |   |  10 |  16 |
	(H12S20)        |  0  |  5  |   |  5  |  11 |   |  11 |  16 |
	(H16S16)        |  0  |  4  |   |  4  |  12 |   |  12 |  16 |
	(H20S12)        |  0  |  3  |   |  3  |  13 |   |  13 |  16 |


	For a (H8S24)16 silk system,
	region		middle5 block  0 6 5 6 5 6 # for soft segment on the left
	region		middle block  6 10 5 6 5 6 # for hard segment
	region		middle2 block  10 16 5 6 5 6 # for soft segment on the right


	The chain length (repeating unit) is determined by the number of repeat unit.
	For 16-unit chain, a chain unit is replicated 16 times along the x direction by using replicate commend. 

	variable        nrepeat equal 16 #chain length
	replicate       ${nrepeat} 1 1

[Simulation Procedure]
	The simulation process consists of the following three main steps:
-	Step 1: The initial configuration needs to be generated.
-	Step 2: The assembly of the initial configuration is simulated.
-	Step 3: An uniaxial tensile test along the x-direction on the assembled silk system is simulated.

[Sample types]
	These steps are performed separately for isotropic and anisotropic silk systems.

	As a convenience, smaller test systems are included while the big systems are identical to those reported in the paper.

	All silk are (H8S24)16 chains.

[Folder Structure]
	Self-explained folder names:
-	SmallSystem-Isotropic
-	SmallSystem-Anisotropic
-	BigSystem-Isotropic
-	BigSystem-Anisotropic
