# Basic system information

During the 2019 GPU Hackathon we will use Zeus (HPE cluster). Node confiugration:
- 4x NVIDIA P100 (Pascal) GPUs connected with NVLINK,
- 2x Intel Xeon Broadwell E5-2680 v4, 14-core each,
- 256GB RAM

Each team has a single node reserved for their exclusive use. Additionally there are 2 nodes for general use, available for all teams with the main purpose of scheduling longer benchmarking runs.  

Documentation: https://support.pawsey.org.au/documentation/display/US/HPC+Systems#HPCSystems-Zeus(HPECluster)
Online video: https://youtu.be/lOAny8Fy9Rc

# Reservation

SLURM is being used on Zeus system. To access your reservation please add "--reservation=RESERVATION_NAME" to sbatch or salloc command. 

**Reservation duration**: from 20 March 2019 (12 am) to 2 April 2019 (12am) 

**List of reservations and teams**:

| Reservation name | Nodes | Access |
| ---------------- | ----- | ------ |
| gpuhackathon     | a087, a088 | gpuhack2019team1, gpuhack2019team2, gpuhack2019team3, gpuhack2019team4, gpuhack2019team5, gpuhack2019team6 | 
| gpuhack2019team1 | a081 | gpuhack2019team1 |
| gpuhack2019team2 | a082 | gpuhack2019team2 |
| gpuhack2019team3 | a083 | gpuhack2019team3 |
| gpuhack2019team4 | a084 | gpuhack2019team4 |
| gpuhack2019team5 | a085 | gpuhack2019team5 |
| gpuhack2019team6 | a086 | gpuhack2019team6 |

# Running jobs

TBD

# Development tools
## Editors
Vim and Emacs are available on Zeus. 

Nano is available within a separate module:

```console
foo@bar:~$ module load nano
foo@bar:~$ nano
```

## Compilers
## CUDA
## OpenACC
## ARM Forge
ARM (www.arm.com) provided us with temporal license available and configured for all teams. The license is for 512 MPI processes and 64 accelerators and should be enough for both development purposes and larger profiling runs.

The ARM Forge suite consists of parallel debugger DDT, profiler MAP (formely known as Allinea DDT and MAP) as well as Performance Reports tool: https://www.arm.com/products/development-tools/server-and-hpc/forge

We recommend to use the ARM Forge Remote client available for free download here: https://developer.arm.com/products/software-development-tools/hpc/downloads/download-arm-forge

Step by step guides for 3 tools are given here:
- ARM MAP: https://support.pawsey.org.au/documentation/display/US/Profiling+with+Arm+MAP
- ARM Performance Reports: https://support.pawsey.org.au/documentation/display/US/Profiling+with+Arm+Performance+Reports
- ARM DDT: https://support.pawsey.org.au/documentation/display/US/Debugging+with+Arm+DDT

Please be aware that during the configuration of the Remote Launch Settings you will need to specify different directory compared to the guides mentioned above. Software is installed for each of the group separately in: ```console /group/gpuhack2019teamN/software/sles12sp3/devel/binary/forge/19.0.3```
(**N** is the team number) 

Module is available after running:
```console
foo@bar:~$ module use /group/gpuhack2019teamN/software/sles12sp3/modulefiles
foo@bar:~$ module load forge/19.0.3
```

# Cloud resources  

TBD
