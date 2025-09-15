---
layout: page
title: Projects
---

---

### _ESC4SHI – Efficient simulation and computation for sea, health and industry_

<p style="margin-bottom:1cm;"></p>

**Principal Investigator**: Stéphane Clain

**Funder**: Portuguese Foundation for Science and Technology (FCT)

**Beneficiaries**: University of Minho (UMinho), University of Coimbra (UCoimbra), Association for the Research and Development of Sciences (FCiências.ID)

**Call**: Call for R&D Projects in All Scientific Domains

**Period**: 14/12/2018 – 13/12/2022 (4 years)

**Reference**: PTDC/MAT-APL/28118/2017, LISBOA-01-0145-FEDER-028118, POCI-01-0145-FEDER-028118

**Abstract and objectives**:

The first part of the project addresses the **efficiency of numerical methods**, focusing on:

* Increasing the **spatial order of convergence**, enabling the same accuracy with significantly fewer unknowns. A major limitation arises with **curved boundaries**, where domain approximations reduce any numerical method to second-order accuracy. **Finite element (FEM)** and **discontinuous Galerkin (DG)** methods employ **isoparametric elements**, which require local transformations, additional computational effort, and complex **curved meshing algorithms**. A novel technique, capable of preserving the optimal convergence order, has been successfully tested for 2D linear convection–diffusion problems in the **finite volume method (FVM)**. We now aim to extend this approach to complex 3D geometries with a broad class of boundary conditions.

* Designing **very high-order implicit time schemes** for unsteady equations. These schemes are not **unconditionally stable**, as the time step remains constrained by the smallest cell size. This typically requires prohibitively small time steps. **Time–space discretisations** provide a promising alternative, enabling unconditional schemes and relaxing stability restrictions. While a 2nd-order implicit formulation for Maxwell’s equations has been proposed in the literature, we aim to extend this strategy through **time–space coupled discretisation**.

* Exploiting modern **hardware architectures**, where personal computers gain performance through **vector units**, **many-core processors**, and **hierarchical cache systems**. Efficient algorithms must be designed to leverage these capabilities. The **alternating direction implicit (ADI)** method decomposes 2D or 3D problems into a series of independent 1D problems solved iteratively. Although recent studies have developed a novel ADI paradigm, they do not yet fully exploit modern hardware. We propose a new ADI formulation specifically optimised for contemporary architectures, enabling many 1D problems to be solved concurrently with available threads, leading to much faster codes.

* Developing novel approaches for **fluid–structure interfaces** and **moving boundaries**. In Eulerian formulations, interfaces cut through cells, leading to inaccuracies in their representation and spurious diffusion. **Smoothed particle hydrodynamics (SPH)** is well-suited for compressible and weakly compressible flows with moving interfaces. However, ensuring **consistency** remains challenging due to the so-called **E0-error**, despite various attempted corrections. We propose a novel **SPH–FVM hybrid formulation**, introducing a new convolution compatible with the space deformation induced by particle displacements. This ensures consistency, better approximating the physics of the problem.

The second part of the project concerns **applications**, namely:

* **Thermoplastic polymer manufacturing processes** demand large amounts of energy for heating, melting, forming, and cooling along the production line. Numerical tools, typically based on 2nd-order FVM, are widely used to predict temperature evolution and guide experimental validation. However, such tools often require **highly refined meshes**, resulting in large computational costs. By developing more efficient and higher-order accurate methods, we aim to enable **real-time simulations** that can be integrated into the **cooling process control loop**, thereby increasing efficiency and reducing energy consumption.

* **Coastal structures** in tsunami-prone regions must be designed to withstand extreme hydrodynamic forces while balancing safety requirements and construction costs. FVM is commonly adopted to simulate large-scale oceanic flows, while **SPH** methods are better suited for the highly nonlinear **tsunami–structure interactions**. However, SPH currently suffers from **lack of consistency** and strong **numerical dissipation**. The proposed development of a consistent SPH formulation will enable a reliable and efficient numerical tool for assessing tsunami impacts on coastal structures.

* The **retina**, as the only visible part of the central nervous system, can be directly imaged using non-invasive optical devices. A common approach to assess the progression of **diabetic macular edema (DME)** and neurodegenerative diseases is to monitor **retinal thickness** via **optical coherence tomography (OCT)**. While OCT distinguishes between healthy and DME patients, it cannot directly capture changes at the cellular scale. Thus, a rigorous study of how **electromagnetic waves** propagate through the retinal layers is required. Previously, we developed a 3D multilayer **Monte Carlo model** of the retina, where the optical properties of each layer were obtained from full-wave solutions of **Maxwell’s equations** using a **DG-FEM** formulation. Building on this, we now aim to develop an advanced OCT computational model based on **time–space explicit DG-FEM methods**, enabling the study of normal ageing and neurodegenerative diseases without relying solely on morphological alterations.
