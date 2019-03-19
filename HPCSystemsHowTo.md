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

# Logging in

You can login to Zeus system with the use of secure shell (SSH):
```console
foo@bar:~$ ssh username@zeus.pawsey.org.au
```

# Running jobs

GPU Hackathon participants can login directly into compute nodes assigned to their team. For instance, members of the gpuhack2019team1 can login directly into a081:
```console
username@zeus:~$ ssh a081
Password:
Access denied by pam_slurm_adopt: you have no active jobs on this node
Last login: Wed Mar 13 08:41:51 2019 from 146.118.36.65
username@a081:~$
```
The "Access denied" message should be disregarded. GPU Hackathon projects are added to exception list of the pam_slurm_adopt which is enabled on Zeus.  

It is also possible to submit jobs to the gpuhackathon reservation. This is mainly dedicated for longer (e.g. profiling) or 2-node runs. To use it specify "--reservation=gpuhackathon" option in the srun command or "#SBATCH --reservation=gpuhackathon" in the queueing script. 

For instructions on how to create queueing scripts and how to use SLURM on Pawsey HPC systems please refer to: 
https://support.pawsey.org.au/documentation/display/US/Job+Scheduling

# Development tools

## Environment

Lmod is used for environemnt management on Zeus system. 
For more information on how to use Lmod please refer to: 
https://support.pawsey.org.au/documentation/display/US/Modules

as well as: 
https://youtu.be/NjCqMTVisEc

## Editors
Vim and Emacs are available on Zeus. 

Nano is available within a separate module:

```console
foo@bar:~$ module load nano
foo@bar:~$ nano
```

## Compilers

There are 3 compiler families available on Zeus:
* GNU compiler: 4.8.5, 5.5.0, 7.2.0
* Intel compiler: 17.0.5
* PGI compiler: 18.3, 19.1

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
