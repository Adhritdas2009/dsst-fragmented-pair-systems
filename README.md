# dsst-fragmented-pair-systems

Code for the paper *Dynamical Sector-Selective Thermalization in Fragmented Pair Systems* by Adhrit Das.

The preprint is on Zenodo, DOI [10.5281/zenodo.23123947](https://doi.org/10.5281/zenodo.23123947). The paper is in its second round of peer review at Physica A.

## What the paper shows

The model is a superconducting-like lattice with correlated pair hopping. Kinetic constraints delete single-particle hopping paths from the many-body graph and leave the pair-hopping paths in place. Exact many-body dynamics up to L = 14 show density memory relaxing while pair memory stays long-lived, which the paper calls Dynamical Sector-Selective Thermalization (DSST). The effect is checked across several constraint rules, with term-ablation controls and a commutator-rate diagnostic.

## What's in the repository

`DSST_code.ipynb` is the full Colab notebook for the project, about 10,500 lines over twelve code cells, meant to run top to bottom.

- Part 1 builds the many-body setup, including the operators, the Hamiltonian, constraint projectors, disorder, boundary conditions and the sparse-matrix tools.
- Part 2 and Phases 3 to 7 add the solvers and diagnostics, like exact diagonalization, Krylov time evolution, pair correlators, level statistics, OTOCs and Krylov complexity.
- Phase 9 is the main CPPC and DSST pipeline, run at L = 8, 10 and 12 with a focused run at L = 14.
- The cell after it is the universality and analytic theory suite. It compares the edge-vacancy, soft edge-vacancy, blockade and pair-preserving constraints and runs the term-ablation controls.
- The commutator-rate calculation comes next and needs the universality cell to have run first.
- The last cell draws the model schematic in Figure 1.

## Running it

The notebook was written in Google Colab with Python 3. Outside Colab, install the dependencies with
