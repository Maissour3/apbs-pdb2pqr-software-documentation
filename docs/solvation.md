# Solvation Free Energy & Electrostatic Surfaces

APBS calculates polar electrostatic contributions to total biomolecular solvation energies by computing the thermodynamic difference between charging molecules in aqueous solvent versus vacuum reference states.

## Energy Component Breakdown

$$\Delta G_{solv} = \Delta G_{polar} + \Delta G_{non-polar}$$

| Component | Physical Mechanism | Calculation Method |
| :--- | :--- | :--- |
| $\Delta G_{polar}$ | Dielectric shielding by water solvent | Finite-element Poisson-Boltzmann solution |
| $\Delta G_{cavity}$ | Cavity formation work in solvent | Solvent-Accessible Surface Area (SASA) |
| $\Delta G_{dispersion}$ | Attractive van der Waals solute-solvent interactions | Numerical volume integration over solvent density |

## Surface Potential Mapping

Calculated electrostatic potential fields can be rendered directly onto solvent-accessible molecular surfaces, mapping positive potential (blue) and negative potential (red) regions in PyMOL or VMD visualization environments.
