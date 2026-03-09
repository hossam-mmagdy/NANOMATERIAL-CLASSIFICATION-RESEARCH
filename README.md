# Nanomaterial Classification Research Framework (NCRF)

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.xxxxx.svg)](https://doi.org/10.5281/zenodo.xxxxx)

> **Publication-Ready Computational Framework for Quantum Confinement Analysis and Machine Learning Classification of Low-Dimensional Nanomaterials**

<p align="center">
  <img src="assets/quantum_confinement_demo.png" width="800" alt="Quantum Confinement Analysis"/>
</p>

## Overview

The **Nanomaterial Classification Research Framework (NCRF)** is a comprehensive, scientifically rigorous Python toolkit designed for the computational analysis, classification, and visualization of low-dimensional nanomaterials (0D, 1D, 2D, 3D). This framework implements first-principles physical models combined with advanced machine learning techniques to enable quantitative structure-property relationship (QSPR) studies in nanoscience.

### Key Features

- **Physics-Based Modeling**: Implements the Brus equation with Coulomb correction for quantum confinement effects
- **Statistical Rigor**: Comprehensive hypothesis testing, effect size calculations, and power analysis
- **Machine Learning Integration**: PCA, t-SNE, clustering algorithms, and Random Forest classification
- **Publication-Quality Visualizations**: Vector-ready figures compliant with Nature/Science journal standards
- **Standards Compliance**: Follows ISO/TS 80004-1, ASTM E56, and ISO/TR 13014 nanotechnology standards

---

## Table of Contents

1. [Scientific Background](#scientific-background)
2. [Installation](#installation)
3. [Quick Start](#quick-start)
4. [Framework Architecture](#framework-architecture)
5. [Physical Models](#physical-models)
6. [Machine Learning Pipeline](#machine-learning-pipeline)
7. [Visualization Standards](#visualization-standards)
8. [Results & Validation](#results--validation)
9. [Citation](#citation)
10. [License](#license)

---

## Scientific Background

### Quantum Confinement Effects

In low-dimensional nanomaterials, quantum confinement leads to size-dependent electronic properties. The framework implements the **Brus Equation** (Effective Mass Approximation):

$$E(R) = E_{bulk} + \frac{\hbar^2\pi^2}{2\mu R^2} - \frac{1.786e^2}{\varepsilon R} - 0.248E_{Ryd}$$

Where:
- $E(R)$: Size-dependent band gap
- $\mu$: Reduced effective mass ($\mu = \frac{m_e^* m_h^*}{m_e^* + m_h^*}$)
- $R$: Nanocrystal radius
- $\varepsilon$: Dielectric constant
- $E_{Ryd}$: Effective Rydberg energy

### Surface Area to Volume Scaling

The framework calculates geometric properties for different morphologies:

| Dimensionality | Geometry | SA:V Scaling |
|---------------|----------|--------------|
| 0D | Sphere | $\propto d^{-1}$ |
| 1D | Cylinder (AR > 5) | $\propto d^{-1}$ (weak) |
| 2D | Slab (t << L) | $\propto t^{-1}$ |
| 3D | Bulk | $\approx$ constant |

---

## Installation

### Requirements

```bash
Python >= 3.8
NumPy >= 1.21.0
SciPy >= 1.7.0
Matplotlib >= 3.4.0
Seaborn >= 0.11.0
Scikit-learn >= 1.0.0
Pandas >= 1.3.0
