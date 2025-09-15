---
layout: page
title: Projects
---

---

### _SIMPAR – Hybrid parallel programming model with domain decomposition for efficient fluid flow simulations_

<p style="margin-bottom:1cm;"></p>

**Principal Investigator**: Ricardo Costa

**Funder**: Portuguese Foundation for Science and Technology (FCT)

**Institution**: University of Minho (UMinho)

**Call**: Advanced Computing Projects Call – 4th Edition (FCT_CPCA_2023_01)

**Period**: 01/08/2024 – 31/07/2025 (1 year)

**Reference**: 2024.07065.CPCA.A1

**DOI**: [https://doi.org/10.54499/2024.07065.CPCA.A1](https://doi.org/10.54499/2024.07065.CPCA.A1)

**Abstract and objectives**:

The proposed research plan aims to develop innovative methods in **computational mechanics** for reliable and efficient (time and energy) simulations of **manufacturing technologies** with advanced materials. These developments aim to contribute to the applicability of computational mechanics tools in the industry, seeking to **optimise industrial processes** in terms of quality, economic viability and environmental sustainability (with reduced material waste and energy consumption). More specifically, the proposed research addresses the development of **novel advanced numerical methods** of high precision, robustness, stability and efficiency for application in **multiphysics and multidomain problems**, with **complex materials** and **intricate geometries**, akin to the manufacturing industry. In particular, spatial and temporal discretisation techniques with a high order of convergence will be investigated, and techniques for solving algebraic systems with high efficiency and scalability in HPC systems will be implemented. The developed codes will be verified and applied to solve real problems of sophisticated manufacturing technologies, such as **additive manufacturing**, **(micro-)injection moulding** and **(micro-)extrusion** of polymers and composites.

The present advanced computing project proposal intends to support the computational tasks planned in a recently approved scientific project within the "Individual Call to Scientific Employment Stimulus" call, whose motivation and objectives are given above. The approved research project is divided into three work packages (WP1 – Discretisation methods of high precision and stability, WP2 – Efficient and highly parallelisable solution algorithms, and WP3 – Applications and transfer of knowledge and technology), covering a comprehensive scope from the theoretical aspects to the code implementation, and taking into account the practical needs of the end-users in the industry. Indeed, the continuous assessment and improvement of the developed method's computational efficiency is crucial for its applicability in demanding engineering applications. In that regard, the exploitation of **HPC systems** will be accomplished with the **parallel implementation** of the developed methods, using **shared-memory** and **distributed-memory programming models** together with domain **decomposition techniques**. Furthermore, the implemented code will be analysed with advanced profiling tools to identify the main bottlenecks and provide essential directions for algorithmic improvements.

In practical terms, the numerical developments are being carried out in the [[FVLib code](https://ricardodpcosta.github.io/fvlib.html)], a library of advanced computational algorithms and numerical methods to solve partial differential equations within the **finite volume philosophy**. This computational library aims to deliver **high-accurate**, **high-performance**, and **high-efficient simulations** of a wide range of physics and mechanics problems in relevant industrial, environmental, and biomedical applications. Currently, the FVLib code multi-processing capabilities are implemented based on the **shared-memory programming model** through the OpenMP application programming interface. It allows the development and deployment of portable and scalable intra-node parallel applications, but cannot take full advantage of modern HPC systems since inter-node communication, demanded to simulate large-scale **engineering applications** on meshes with several millions of cells, requires a **distributed-memory programming model**.

The first objective of the present advanced computing project proposal is to implement a **distributed-memory parallel programming model** in the FVLib code through the message-passing interface (MPI) paradigm. MPI has become a reliable and widely used standard for writing portable scalable large-scale parallel applications in modern HPC systems and is available in several open-source implementations (such as OpenMPI and MPICH). The second objective of the present advanced computing project proposal is to analyse a **hybrid shared-memory/message-passing programming model**, often discussed in the literature as a method for achieving better application performance on clusters of distributed-memory systems. Since the FVLib code already provides a shared-memory parallelisation, **combining OpenMP and MPI** (and therefore the shared-memory and message-passing models) shall be a straightforward step, although it requires careful analysis and optimisation.
