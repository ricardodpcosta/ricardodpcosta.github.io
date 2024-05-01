---
layout: page
title: FVLib code
---

<p style="margin-bottom: 1cm;"></p>

The FVLib code is a library of advanced computational algorithms and numerical methods to solve partial differential equations (PDEs) within the **finite volume philosophy**. The project aims to deliver **high-accurate**, **high-performance**, and **high-efficient** simulations of a wide range of physics and mechanics problems in relevant industrial, environmental, and biomedical applications.

### Features

These are the main capabilities of the FVLib code:

#### **Modern object-oriented Fortran (2003/2008 standards)**

The FVLib code is programmed in modern Fortran (2003/2008 standards) with an object-oriented paradigm for better code reuse and maintenance. Its architecture is organised in three levels:

- **core level**: linear algebra algorithms, input/output, mesh and field handlers, etc.
- **apps level**: specific model solvers, pre-processing, and post-processing tools.
- **case level**: geometry files, mesh files, parameters files and scripts setup.

#### **Very high-order accuracy in space and time**

The discretisation methods implemented in the FVLib code are highly accurate in space and time, effectively achieving up to the eighth-order of convergence. Comprehensive benchmarking proves that high-order accurate schemes benefit from a better trade-off between accuracy and efficiency than the counterpart lower-order accurate ones. Hence, this property can be exploited in two different ways:

- **Improving accuracy**: for the same discrete geometrical representation level, high-order accurate schemes provide <span style="color:blue">_significantly more accurate solutions_</span> than those obtained with the traditional first- and second-order accurate schemes.

- **Enhancing efficiency**: for the same approximate solution accuracy level, high-order accurate schemes provide <span style="color:blue">_significantly more efficient computations_</span> than those of the traditional first- and second-order accurate schemes.

#### **Unstructured meshes with general element shapes**

- for complex geometries in real applications

#### **Arbitrary curved domains with piecewise linear meshes**

- for complex geometries in real applications


#### **Parallel computing for HPC environments**

The FVLib code  take advantage of modern HPC systems




Currently, the following problems can be solved in the FVLib code:

- Convection-diffusion problems for heat and species transfer
- Conjugate heat transfer with solid/solid and solid/fluid interfaces
- Incompressible isothermal fluid flows with the Euler/Stokes/Navier-Stokes formulation
- Incompressible non-isothermal fluid flows with the Euler/Stokes/Navier-Stokes formulation
- Incompressible non-Newtonian fluid flows with the Stokes/Navier-Stokes formulation

### 2. Contributing

The FVLib code is not currently an open-source project. However, anyone willing to contribute to the project and/or making use of its potentialities on a collaboration basis is welcome. Please, [contact me](mailto:rcosta@dep.uminho.pt).
