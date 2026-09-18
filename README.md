# XC100

XC100 is a dataset of 100 atomic and molecular systems containing wavefunction-derived exchange-correlation energies for the development and benchmarking of density functional approximations.

This repository accompanies ongoing work from the Zimmerman Group at the University of Michigan.

## Repository contents

* **`XC100_dataset.csv`** — XC100 exchange-correlation dataset for systems 001–100.
* **`molecule_mapping.txt`** — mapping between the numerical system IDs and molecular/species names.
* **`XC100_structures.zip`** — molecular geometries for all 100 systems in XYZ format.
* **`CI_derived_KS_AO_density_matrices/`** — CI-derived Kohn–Sham AO density matrices in the cc-pVTZ basis for systems 001–100.

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

## CI-derived Kohn–Sham AO density matrices

The CI-derived Kohn–Sham AO density matrix for each XC100 system is provided in the cc-pVTZ basis. Each numbered subdirectory corresponds to the matching XC100 system identifier and contains a `Paoks` file.

The matrices use real spherical harmonic atomic orbitals. Within each angular-momentum shell, the basis functions are ordered by increasing \(m\) index, from \(m=-l\) to \(m=+l\):

* `s`: \(m = 0\)
* `p`: \(m = -1, 0, +1\)
* `d`: \(m = -2, -1, 0, +1, +2\)
* `f`: \(m = -3, -2, -1, 0, +1, +2, +3\)

## Citation

A citation to the associated manuscript/preprint will be added upon public release of the repository.
