# Method of Moments for Microstrip Transmission Line Analysis

## Overview

This repository contains a Python implementation of the Method of Moments (MoM) for the electrostatic analysis of a microstrip transmission line.

The implementation formulates the integral equation for the surface charge density, discretizes the conducting strip using pulse basis functions, assembles the impedance matrix, solves the resulting linear system, and computes the characteristic impedance of the transmission line.

The notebook also evaluates the convergence of the characteristic impedance as the number of basis functions increases.

## Features

* Implementation of the Method of Moments for a microstrip transmission line.
* Discretization of the conducting strip with pulse basis functions.
* Numerical construction of the impedance matrix.
* Solution of the linear system for the surface charge density.
* Computation of the capacitance per unit length.
* Computation of the characteristic impedance.
* Convergence analysis with different numbers of basis functions.

## Numerical Model

The implementation considers a microstrip transmission line defined by the following parameters:

* Strip width.
* Dielectric thickness.
* Substrate width.
* Relative permittivity.
* Vacuum permittivity.

The Green's function is evaluated through a truncated series expansion. The conducting strip is divided into `M` segments, and pulse basis functions are applied to approximate the surface charge density.

After solving the linear system, the implementation computes:

* Surface charge density coefficients.
* Capacitance per unit length with dielectric.
* Capacitance per unit length in air.
* Characteristic impedance.

## Project Structure

```text
.
├── lista_método_dos_momentos_v2 (1).ipynb
└── README.md
```

## Requirements

* Python 3
* NumPy
* SciPy
* Matplotlib

Install the required packages with:

```bash
pip install numpy scipy matplotlib
```

## Usage

Open the notebook and execute the cells in order.

The notebook performs the following steps:

1. Defines the transmission line geometry and material properties.
2. Builds the Method of Moments impedance matrix.
3. Solves the linear system for the surface charge density.
4. Computes the capacitance per unit length.
5. Computes the characteristic impedance.
6. Repeats the computation for different numbers of basis functions.
7. Plots the convergence of the characteristic impedance.

## Output

The notebook produces:

* Surface charge density coefficients.
* Capacitance per unit length.
* Characteristic impedance.
* Convergence plot of the characteristic impedance as a function of the number of basis functions.
* Percentage error relative to the reference characteristic impedance.

## License

This project is licensed under the MIT License.
