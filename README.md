# UEES 207: Geophysical Processes — Assignment II

## Overview
This repository contains the data and supporting scripts for Assignment II. The task is to develop a numerical code to compute and visualize the radial component of the Earth's magnetic field ($\mathbf{B}_r$) at the **Core-Mantle Boundary (CMB)** utilizing spherical harmonic expansion.

## Physical Parameters
For all calculations, use the following reference values:
* **Earth Surface Radius ($a$):** 6371 km
* **CMB Radius ($r$):** 2886 km
* **Maximum Degree ($l_{max}$):** 10



---

## Data Dictionary
The following files are required to complete the assignment:

| File | Description |
| :--- | :--- |
| `data.mat` | A MATLAB workspace file containing a structure or matrix with Gauss coefficients ($g_l^m, h_l^m$) organized by degree $l$ and order $m$. |
| `data.txt` | A plain-text version of the Gauss coefficients for Python users. |
| `coastlines.mat` | High-resolution geographical reference data containing `coastlat` and `coastlon` vectors for continent outlines. |
| `bwr.m` | A custom MATLAB function to generate a Blue-White-Red colormap centered at zero. |

---

## Technical Requirements

### 1. Mathematical Implementation
The radial field $\mathbf{B}_r$ must be computed using the appropriate spherical harmonic derivative. You are required to use **Schmidt-normalized** associated Legendre functions.
* **MATLAB:** Use the `legendre(l, x, 'sch')` flag.
* **Python:** Use the `SHTOOLS` library or equivalent normalization logic.

### 2. Visualization
* **Projection:** The final field must be rendered using a **Hammer projection**.
* **Geographical Reference:** Continent outlines from `coastlines.mat` must be projected and overlaid on the magnetic field.
* **Colormap:** Use the provided `bwr.m` script to ensure positive and negative flux patches are clearly distinguished with white at $0$ nT.



---

## Benchmarks
To verify your code, compare your outputs against the four benchmark figures included in the repository:
1.  **Dipole Field:** $l=1, m=0$
2.  **Quadrupole Case:** $l=2, m=2$
3.  **Octupole Case:** $l=3, m=1$
4.  **Full Reconstruction:** Combined field up to $l=10$

## Submission
Your final submission should include:
* The complete source code (MATLAB `.m` or Python `.py`) with proper comments.
* The four generated plots corresponding to the benchmarks listed above.

---
**Course:** UEES 207 Geophysical Processes  
