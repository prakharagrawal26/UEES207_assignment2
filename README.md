# UEES 207: Geophysical Processes — Assignment II

## Overview
This repository contains the necessary data, scripts, and benchmark results for the second assignment. The objective is to develop a numerical code to compute and visualize the radial component of the Earth's magnetic field ($\mathbf{B}_r$) at the **Core-Mantle Boundary (CMB)** using spherical harmonic expansion.

## Assignment Description
Write a numerical code in MATLAB or Python to compute the radial magnetic field at the CMB based on the provided Gauss coefficients. The visualization should accurately reflect the magnetic field morphology at the CMB.

### Physical Parameters
* **Surface Radius ($a$):** 6371 km
* **CMB Radius ($r$):** 2886 km
* **Projection:** Hammer Projection
* **Features:** Include coastline contours for geographical reference.



---

## Repository Contents

| File | Description |
| :--- | :--- |
| [`data.mat`](https://github.com/prakharagrawal26/UEES207_assignment2/blob/main/data.mat) | Gauss coefficients ($g_l^m$ and $h_l^m$) in MATLAB format (up to degree $l=10$). |
| [`data.txt`](https://github.com/prakharagrawal26/UEES207_assignment2/blob/main/data.txt) | Gauss coefficients in plain text format for Python/other environments. |
| [`bwr.m`](https://github.com/prakharagrawal26/UEES207_assignment2/blob/main/bwr.m) | Custom "Blue-White-Red" colormap script required for visualization. |
| `l1m0.jpeg`, `l2m2.jpeg`, etc. | Benchmark figures to verify implementation accuracy. |

---

## Implementation Hints

### Spherical Harmonics & Normalization
The radial component $B_r$ is derived from the spherical harmonic expansion of the magnetic scalar potential. It is essential to use **Schmidt-normalized** associated Legendre functions.

* **MATLAB:** Refer to the [`legendre`](https://in.mathworks.com/help/matlab/ref/legendre.html) function (use the `'sch'` option).
* **Python:** Refer to the [`SHTOOLS`](https://shtools.github.io/SHTOOLS/python-legendre-functions.html#schmidt-normalized) legendre functions documentation.

---

## Benchmarks
To verify your implementation, your code should produce visualizations consistent with the provided benchmark images in the repository for these specific cases:
1.  $l=1, m=0$
2.  $l=2, m=2$
3.  $l=3, m=1$
4.  Full field reconstruction up to degree $l=10$



## Submission Requirements
1.  **Source Code:** Your well-commented MATLAB (.m) or Python (.py) script.
2.  **Plots:** The four generated figures corresponding to the benchmark cases mentioned above.

---
**Course:** UEES 207 Geophysical Processes  
