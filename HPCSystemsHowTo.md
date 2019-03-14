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
## Compilers
## CUDA
## OpenACC
## ARM Forge

# Cloud resources  

TBD
