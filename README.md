# SID_validation
# author: Eric Frizzell
# efrizz@umd.edu

# The files in this repository allow you to create long, slender granular assemblies which can then be settled, tapped, and shocked.

# The general flow is to create a bed using ./bed_prep/in.pour which produces a binary restart file ('restart.static'). Then the restart file can be settled using ./tap/in.settle and then use the settled bed in a shock simulation (shock/in.shock*). Beds can also be tapped to acheive a different packing fraction using ./tap/in.tap

# To run these files, you will need to install LIGGGHTS, an open source CFD-DEM solver. Download LIGGGHTS at:
# https://www.cfdem.com/download-liggghtsr-public

# You will need to compile LIGGGHTS in order to produce a shell script / executable (something like lmp_auto, or lmp_mpi). This executable is used when launching any of the LIGGGHTS job scripts, an example of which is provided in ./shock/job_shock.sub. Our scripts are written with message passing interface (MPI) enabled, so you will need to have this available as well.

# The results of each job script are output files that will appear in post/ and post_computes/ directories within the folder where the job was run. The post files in post/ can be visualized using Ovito, an open source visualization tool:
# https://www.ovito.org/

# Once you have downloaded and installed Ovito, you can load the desired post files to create images and videos with various filters. Note that the post_computes/ output contain entries for every collisional neighbor for every particle at the output timestep and must be further analyzed to generate an average or total overlap per particle.
