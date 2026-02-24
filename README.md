## UEES 207: Geophysical Processes - Assignment II

### Problem Statement
Develop a numerical code (e.g., in MATLAB or Python) to compute and visualize the radial component of the magnetic field, $B_r$, at the Earth's Core-Mantle Boundary (CMB). The visualization must utilize spherical harmonic expansion based on the provided Gauss coefficients.



### Physical Parameters
Use the following reference values for all calculations:
* **Surface Radius ($a$):** 6371 km
* **CMB Radius ($r$):** 2886 km
* **Maximum Degree ($l_{max}$):** 10

### File Descriptions
The following files are provided in this repository for the assignment:
* **`data.mat` / `data.txt`**: Magnetic field data containing Gauss coefficients ($g, h$) up to degree 10.
* **`coastlines.mat` / `coastlines.txt`**: Geographical reference data for continent outlines.
* **`bwr.m`**: Custom colormap script required for MATLAB visualizations.
* **Benchmark Figures**: Reference images (e.g., `l1m0.jpeg`) to verify your code output.

### Magnetic Field Data Organization
The Gauss coefficients are organized into four columns:

| Column | Parameter | Description |
| :--- | :--- | :--- |
| 1 | $l$ | Spherical harmonic degree |
| 2 | $m$ | Spherical harmonic order |
| 3 | $g$ | Gauss coefficient $g_l^m$ |
| 4 | $h$ | Gauss coefficient $h_l^m$ |

### Technical Requirements
* **Normalization:** Use Schmidt-normalized associated Legendre functions.
* **Projection:** Visualizations must be rendered using a **Hammer projection**.
* **Reference:** Include coastline contours from the provided files for geographical context.
* **Colormap:** Use the provided `bwr.m` script to ensure a white center at 0 nT.



### Final Submission
Your submission must include:
1.  **Source Code:** Fully commented MATLAB (`.m`) or Python (`.py`) script.
2.  **Generated Plots:** Four high-resolution plots corresponding to the benchmark cases ($l=1, m=0$; $l=2, m=2$; $l=3, m=1$; and the full reconstruction up to $l=10$).

---
**Course:** UEES 207 Geophysical Processes
