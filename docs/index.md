# Adaptive Poisson-Boltzmann Solver (APBS) & PDB2PQR

Welcome to the documentation for the Adaptive Poisson-Boltzmann Solver (APBS) and PDB2PQR software package. This suite provides state-of-the-art computational tools for evaluating the electrostatic and solvation properties of complex biomolecular assemblies.

## The Poisson-Boltzmann Equation

APBS models continuum biomolecular electrostatics by solving the non-linear or linearized Poisson-Boltzmann equation:

$$\nabla \cdot [\epsilon(r) \nabla \phi(r)] - \kappa^2(r) \sinh[\phi(r)] = -4\pi \rho_f(r)$$

Where $\epsilon(r)$ represents the spatial dielectric coefficient, $\phi(r)$ is the electrostatic potential, $\kappa(r)$ is the Debye-Huckel screening parameter, and $\rho_f(r)$ is the fixed molecular charge distribution.

## Workflow Pipeline

1. **PDB2PQR Stage:** Ingest raw Protein Data Bank (PDB) coordinates, assign missing hydrogen atoms, optimize hydrogen-bonding networks, and calculate atomic partial charges.
2. **Discretization Stage:** Map molecular volumes and dielectric boundaries onto adaptive Cartesian finite-element grids.
3. **Solver Stage:** Solve discretized linear systems using conjugate gradient or multigrid iterative algorithms.
4. **Analysis Stage:** Compute electrostatic solvation free energies and generate 3D potential surface maps.
