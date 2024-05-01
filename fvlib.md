---
layout: page
title: FVLib code
---

### 1. Description

The FVLib code is a library of advanced computational algorithms and numerical methods to solve partial differential equations (PDEs) within the **finite volume philosophy**. The project aims to deliver **high-accurate**, **high-performance**, and **high-efficient** simulations of a wide range of physics and mechanics problems in relevant industrial, environmental, and biomedical applications.

### Features

These are the main capabilities of the FVLib code:

### <span style="color:blue">**Modern object-oriented Fortran (2003/2008 standards)**</span>

The FVLib code is programmed in modern Fortran (2003/2008 standards) with an object oriented paradigm for better code reuse and maintenance. Its architecture is organised in three levels:

- **core level**, the general-purpose functions and routines (linear algebra algorithms, IO handlers, mesh handlers, field handlers, etc.)
- **applications level**, the specific model solvers as well as pre- and post-processing tools
- **case level**, the parameters files and scripts setup.

#### <span style="color:blue">**Very high-order accuracy in space and time**</span>

- *High-scalability with multi-threading execution* - to take advantage of modern HPC systems
- *Unstructured meshes with general element shapes* - for complex geometries in real applications
- *Very high-order of convergence both in space and time* - for highly-accurate and reliable solutions

Currently, the following problems can be solved in the FVLib code:

- Convection-diffusion problems for heat and species transfer
- Conjugate heat transfer with solid/solid and solid/fluid interfaces
- Incompressible isothermal fluid flows with the Euler/Stokes/Navier-Stokes formulation
- Incompressible non-isothermal fluid flows with the Euler/Stokes/Navier-Stokes formulation
- Incompressible non-Newtonian fluid flows with the Stokes/Navier-Stokes formulation

### 2. Contributing

The FVLib code is not currently an open-source project. However, anyone willing to contribute to the project and/or making use of its potentialities on a collaboration basis is welcome. Please, [contact me](mailto:rcosta@dep.uminho.pt).
