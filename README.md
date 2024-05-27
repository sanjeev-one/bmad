# Particle Accelerator Simulation for FACET-II using bmad / l1 l2 phase scans 

## Overview
This repository provides a guide to setting up and utilizing various Python libraries and tools to simulate the beam dynamics in a particle accelerator, specifically for the FACET-II facility. The scripts included demonstrate the process of initializing the simulation environment, running beam dynamics simulations, and visualizing the results.

## Environment Setup
To begin, ensure you have Anaconda or Miniconda installed for managing packages and environments. Follow these steps to create a new environment and install the required packages:

```bash
conda create --name facet_env python=3.9
conda activate facet_env
conda install -c conda-forge bmad pytao openpmd-beamphysics numpy matplotlib pandas
```

## Libraries and Tools
The main libraries used in these scripts include:

- `pytao`: An interface to the Tao accelerator simulation program.
- `numpy`: For numerical operations.
- `matplotlib`: For plotting and visualization.
- `pandas`: For handling structured data.
- `pmd_beamphysics`: For handling particle data and beam physics calculations.

## Environment Variable
Set the `FACET2_LATTICE` environment variable to specify the directory containing the FACET-II lattice files necessary for simulation.

## Helper Functions
The repository includes several helper functions to facilitate the generation of visual representations of the accelerator’s lattice and to perform sorting and plotting operations specific to the facility’s layout.

## Initializing Tao
Initialize the Tao simulation environment with a specific lattice file from the `FACET2_LATTICE` directory. This prepares Tao for performing simulations and calculations on the accelerator model.

## Plotting Twiss Functions
Retrieve and plot Twiss parameters along the accelerator length. Twiss parameters are fundamental in understanding the beam’s transverse dynamics.

## Particle Tracking
Prepare for and execute particle tracking simulations, both without and with considerations for Coherent Synchrotron Radiation (CSR) effects. This involves:

- Initializing a beam of particles.
- Matching their properties to ensure realistic simulation conditions.
- Executing the tracking through the lattice and analyzing the results.

## Visualizing Results
Several plots are generated to visualize the outcomes of simulations, such as the evolution of beam parameters along the accelerator and the final phase space distributions of the particles. This is crucial for understanding the beam behavior and the impact of various accelerator components and settings.

## Double Loop Scan in the `1_l2_phase_scan` Folder
In the `1_l2_phase_scan` folder, there is a double for-loop scan that varies both L1 and L2 phases. This allows for comprehensive testing and visualization of the impact of different phase settings on beam dynamics.

### Scan Process
The scan process involves looping over predefined ranges for L1 and L2 phases. Each combination of L1 and L2 phases is used to run a simulation, and the results are logged and analyzed. If an error occurs during any simulation step, it is caught and displayed for troubleshooting.

### Matrix Plot Visualization
A matrix plot is generated to display all the scan results in a grid format. The plot shows:

- Columns: Representing increasing L2 phase.
- Rows: Representing increasing L1 phase.

This visual representation makes it easy to compare the effects of different phase combinations on the beam dynamics.

## Running the Code
To run the scripts successfully, ensure that all paths and environment variables are correctly set up according to your computational environment. The scripts are tailored for users with a working knowledge of accelerator physics and simulation tools.

## Adaptation for Other Facilities
While the scripts are specific to FACET-II, the general approach and many of the functions can be adapted for simulations of other particle accelerators. Adjustments would be needed to accommodate the specific lattice configuration, component definitions, and desired simulations of the target facility.

## Conclusion
This repository provides a detailed guide to setting up and running beam dynamics simulations using the FACET-II facility. By following the steps outlined and utilizing the provided scripts, users can perform comprehensive simulations and visualize the results effectively.
