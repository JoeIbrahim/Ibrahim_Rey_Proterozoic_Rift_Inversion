# Numerical Experiment Scripts  
### *Used in:*  
**A new geodynamic framework for Proterozoic rifting and inversion**  
*Y. Ibrahim and P. F. Rey*  

---

##  Overview

This repository contains the Python scripts used to run the **MT600** and **MT800** geodynamic experiments with the **Underworld 2 / UWGeodynamics** framework.  

---

## Computational Environment

The models were run using:

- **Underworld 2.15** – [DOI: 10.5281/zenodo.10976370](https://doi.org/10.5281/zenodo.10976370) and tested to work with **Underworld 2.16** – [DOI: 10.5281/zenodo.1436039](https://doi.org/10.5281/zenodo.1436039)  
- **Hardware:** High-performance computing clusters utilizing 1–2 CPU nodes (36–96 cores).  

### Requirements
Only **Underworld 2** and its dependencies are required.  
Installation and setup guides are available at:  
- [Underworld 2 GitHub Repository](https://github.com/underworldcode/underworld2)  
- [Official Documentation](https://underworld2.readthedocs.io/en/latest/)  

---

## First run these scripts for rifting.

| Experiment | Moho Temperature | Tectonic Setting |
|-------------|------------------|--------------|
| **MT600_Rift.py** | Geotherm delivers Moho Temperature of 600 °C | Narrow rift |
| **MT800_Rift.py** | Geotherm delivers Moho Temperature of 800 °C | Wide rift |

These scripts only differ in thermal structure and therefore also the initial lithosphere/asthenosphere boundary depth.

## Use these scripts to restart the experiment in either tectonic quiescence or compression

| Experiment | Tectonic Setting |
|-------------|--------------|
| **MT600_Qsc.py** | Tectonic quiescence post narrow rift |
| **MT800_Qsc.py** | Tectonic quiescence post wide rift |
| **MT600_Orogen.py** | Contraction of the narrow rift |
| **MT800_Orogen.py** | Contraction of the wide rift |

For example, to run a narrow rift experiment with 8 m.y. of rifting, 60 m.y. of tectonic quiescence, and 8 m.y. of contraction you must:
1) run MT600_Rift.py for 8 m.y.
2) run MT600_Qsc.py for 60 m.y.
3) run MT600_Orogen.py for 8 m.y.

Refer to the underworld documentation for more information on running Underworld and restarting models. 

- [Underworld documentation](https://underworld2.readthedocs.io/en/latest/)  
---

## Visualization

Model outputs were post-processed and visualized using **[ParaView](https://www.paraview.org)**, an open-source scientific visualization software.




