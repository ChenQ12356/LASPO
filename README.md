# LASPO

This repository provides the source code and experimental data for the paper:

**Learning-based Adaptive Selection of Preference and Operator for Constrained Multi-objective Optimization**

LASPO is a constrained multi-objective evolutionary algorithm that uses a Q-learning-based neural approximator to adaptively select preference strategies and reproduction operators according to the current evolutionary state.

## Repository Structure

The repository is organized as follows:

- `Code/`: Source code of LASPO and the scripts required to run the experiments.
- `Experimental_Settings/`: Parameter settings, benchmark configurations, and random seeds used in the experiments.
- `Reference_Data/`: Reference sets used for IGD calculation and reference points used for HV calculation.
- `Raw_Results/`: Raw IGD, HV, and runtime results obtained from all independent runs.

## Requirements

The experiments are implemented in MATLAB based on PlatEMO.

- MATLAB: [MATLAB version]
- PlatEMO: [PlatEMO version]
- Operating system: [Operating system]
- Processor: AMD Ryzen 9 9950X
- Population size: 100
- Maximum number of function evaluations: 100,000

## Running LASPO

1. Download and install PlatEMO.
2. Copy the files in `Code/` to the corresponding directories of PlatEMO.
3. Start MATLAB and add PlatEMO to the MATLAB search path.
4. Run LASPO through the PlatEMO graphical interface or command line.

An example command is:

```matlab
platemo('algorithm', @LASPO, 'problem', @DASCMOP1, ...
        'N', 100, 'maxFE', 100000);
