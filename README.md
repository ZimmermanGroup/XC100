# XC100

XC100 is a dataset of 100 atomic and molecular systems containing wavefunction-derived exchange-correlation energies for the development and benchmarking of density functional approximations.

This repository accompanies ongoing work from the Zimmerman Group at the University of Michigan.

## Repository contents

* **`XC100_dataset.csv`** — XC100 exchange-correlation dataset for systems 001–100.
* **`molecule_mapping.txt`** — mapping between the numerical system IDs and molecular/species names.
* **`XC100_structures.zip`** — molecular geometries for all 100 systems in XYZ format.
* **`CI_derived_KS_AO_density_matrices/`** — CI-derived Kohn–Sham one-particle reduced density matrices (1-RDMs) in the cc-pVTZ AO basis for systems 001–100.

## Dataset columns

| Column                    | Description                                                             |
| ------------------------- | ----------------------------------------------------------------------- |
| `System`                  | Three-digit XC100 system identifier                                     |
| `Exc_TZ`                  | Exchange-correlation energy at the cc-pVTZ level                        |
| `TZ_correlation`          | cc-pVTZ correlation energy                                              |
| `QZ_correlation`          | cc-pVQZ correlation energy                                              |
| `CTZ_correlation`         | cc-pCVTZ correlation energy                                             |
| `delta_Riemann_QZ_to_CBS` | Riemann-extrapolated correction from QZ to the complete-basis-set limit |
| `Exc_comp`                | Final composite exchange-correlation energy                             |
| `Ex_TZ`                   | Exchange energy obtained from the cc-pVTZ inversion                     |

All energies are reported in Hartree.

The `Exc_comp` values correspond to the final composite, Riemann-corrected exchange-correlation energies.

## Structures and system IDs

Structures are provided as individual XYZ files named according to the XC100 system identifier:

```text
001.xyz
002.xyz
...
100.xyz
```

The corresponding species names are provided in `molecule_mapping.txt`.

## CI-derived Kohn–Sham 1-RDMs

The CI-derived Kohn–Sham one-particle reduced density matrix (1-RDM) for each XC100 system is provided in the cc-pVTZ AO basis. Each numbered subdirectory corresponds to the matching XC100 system identifier and contains a `Paoks` file.

## Citation

If you use the XC100 dataset in your research, please cite:

> Vaibhav Khanna and Paul M. Zimmerman,  
> *XC100: A Wavefunction-Derived Exchange-Correlation Energy Dataset for Atomic and Molecular Species*,  
> arXiv:2609.22490 [physics.chem-ph] (2026).

```bibtex
@misc{khanna2026xc100wavefunctionderivedexchangecorrelationenergy,
      title={XC100: A Wavefunction-Derived Exchange-Correlation Energy Dataset for Atomic and Molecular Species},
      author={Vaibhav Khanna and Paul M. Zimmerman},
      year={2026},
      eprint={2609.22490},
      archivePrefix={arXiv},
      primaryClass={physics.chem-ph},
      url={https://arxiv.org/abs/2609.22490},
}
