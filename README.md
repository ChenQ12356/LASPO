This repository provides the source code and experimental data for the paper:

**Learning-based Adaptive Selection of Preference and Operator for Constrained Multi-objective Optimization**

## Repository Structure

The repository is organized as follows:

- `Code/`: Source code of LASPO and the scripts required to reproduce the experiments.
- `Experimental_Settings/`: Parameter settings and benchmark configurations used in the experiments.
- `Reference_Data/`: Reference sets used for IGD calculation and reference points used for HV calculation.
- `Raw_Results/`: Raw IGD, HV, and runtime results obtained from all independent runs.

## Requirements

The experiments are conducted in MATLAB based on PlatEMO.

- Platform: PlatEMO 4.15
- Operating system: Windows Server 2019
- Processor: Intel(R) Xeon(R) Platinum 8375C @ 2.90 GHz
- Memory: 512 GB RAM
- MATLAB version: R2021a
- Population size: 100
- Maximum number of function evaluations: 100,000

The implementations of the compared algorithms and benchmark problems are provided by the PlatEMO platform.

## Running LASPO

1. Download and install PlatEMO.
2. Copy the files in `Code/` to the corresponding directories of PlatEMO.
3. Start MATLAB and add PlatEMO to the MATLAB search path.
4. Run LASPO through the PlatEMO graphical interface or command line.

An example command is:

```matlab
platemo('algorithm', @LASPO, 'problem', @DASCMOP1, ...
        'N', 100, 'maxFE', 100000);
