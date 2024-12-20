---
layout: page
title: Projects
---

<p style="margin-bottom:1cm;"></p>

<div class="message">
  List of funded projects as principal investigator. Please refer to the <i>Curriculum Vitae</i> for a complete list.
</div>

---

### _SIMPRO – Efficient computation and simulation of complex materials in advanced manufacturing processes_

<p style="margin-bottom:1cm;"></p>

**Funder**: Portuguese Foundation for Science and Technology (FCT)

**Call**: Individual Call to Scientific Employment Stimulus - 6th Edition

**Period**: 17/09/2024 – 16/09/2030

**Budget**: TBD

**Abstract and objectives**:

The application of **computational mechanics tools** in the industry has seen remarkable growth in the past years, fostering technological innovation towards cutting-edge **manufacturing processes** with **complex materials**. Moreover, as sustainability has become an essential concern in any economic sector, the reasons for further promoting computer-aided approaches are uncountable. Indeed, the design and optimisation of manufacturing processes are traditionally performed solely through experimentation in time-consuming trial-and-error procedures, with large amounts of **material waste** and **energy consumption**. Contrarily, computer-aided approaches promote increased **resource-use efficiency** (both of material and energy) and foster clean and environmentally sound technologies and industrial processes. On the other side, the development of high-performance, complex materials (such as polymers and composites), with improved mechanical and thermal properties, for critical parts and components (from biomedical to aerospace) demands sophisticated, cutting-edge manufacturing technologies. In polymer processing, the **viscoelastic response** of **molten polymers** to deformation, together with the **thermal dependence**, promotes a counter-intuitive rheological behaviour and makes the experimental-based optimisation of manufacturing processes substantially more challenging. In particular, emerging technologies, such as additive manufacturing, micro-injection moulding, and micro-extrusion, raise considerable difficulties as the elastic effects become more dominant in low mass flows at large deformation rates. Similarly, the complex properties of **engineered composite materials**, different from the simple individual components, make their structural and thermal performance difficult to predict. The intricate behaviour of these materials and the limitations of the experimental approaches emphasise the benefits of applying computational mechanics tools.

The current so ftware for computational mechanics still relies on **classical and simple numerical methods**, typically with **low accuracy** and **poor performance**, uneven with the ever-increasing complex problems akin to advanced manufacturing technologies with complex materials. Therefore, time- and energy-consuming simulations in powerful hardware are required to achieve reliable results, which substantially constrains the application of computational modelling approaches and their economic viability and sustainability advantages. **_The present research aims to develop innovative novel numerical methods and computational codes for computational mechanics problems, targeting sophisticated manufacturing technologies with complex materials_**. Highly accurate discretisation techniques and robust solution procedures, enhanced with optimised algorithms and parallel implementations, will enable highly efficient (time and energy) simulations and provide reliable results, fostering a sustainable technological innovation of industries.

---

### _SIMPRO-CPCA – Efficient computation and simulation of complex materials in advanced manufacturing processes_

<p style="margin-bottom:1cm;"></p>

**Funder**: Portuguese Foundation for Science and Technology (FCT)

**Call**: Advanced Computing Projects Call – 4th Edition - A1 Development Access (Round D)

**Period**: 01/08/2024 – 31/07/2025

**Budget**: TBD

**Abstract and objectives**:

**_The proposed research plan aims to develop innovative methods in computational mechanics for reliable and efficient (time and energy) simulations of manufacturing technologies with advanced materials_**. These developments aim to contribute to the applicability of computational mechanics tools in the industry, seeking to **optimise industrial processes** in terms of quality, economic viability and environmental sustainability (with reduced material waste and energy consumption). More specifically, the proposed research addresses the development of **novel advanced numerical methods** of high precision, robustness, stability and efficiency for application in **multiphysics and multidomain problems**, with **complex materials** and **intricate geometries**, akin to the manufacturing industry. In particular, spatial and temporal discretisation techniques with a high order of convergence will be investigated, and techniques for solving algebraic systems with high efficiency and scalability in HPC systems will be implemented. The developed codes will be verified and applied to solve real problems of **sophisticated manufacturing technologies**, such as additive manufacturing, (micro-)injection moulding and (micro-)extrusion of polymers and composites.

**_The present advanced computing project proposal intends to support the computational tasks planned in a recently approved scientific project_** within the "Individual Call to Scientific Employment Stimulus" call, whose motivation and objectives are given above. The approved research project is divided into three work packages (WP1 – **Discretisation methods of high precision** and stability, WP2 – **Efficient and highly parallelisable solution algorithms**, and WP3 – **Applications and transfer of knowledge and technology**), covering a comprehensive scope from the theoretical aspects to the code implementation, and taking into account the practical needs of the end-users in the industry. Indeed, the continuous assessment and improvement of the developed method's computational efficiency is crucial for its applicability in demanding engineering applications. In that regard, the exploitation of **HPC systems** will be accomplished with the **parallel implementation** of the developed methods, using **shared-memory** and **distributed-memory programming models** together with domain **decomposition techniques**. Furthermore, the implemented code will be analysed with advanced profiling tools to identify the main bottlenecks and provide essential directions for algorithmic improvements.

In practical terms, the numerical developments are being carried out in the [[FVLib code](https://ricardodpcosta.github.io/fvlib.html)], a library of **advanced computational algorithms** and **numerical methods** to solve partial differential equations within the **finite volume philosophy**. This computational library aims to deliver **high-accurate**, **high-performance**, and **high-efficient simulations** of a wide range of physics and mechanics problems in relevant industrial, environmental, and biomedical applications. Currently, the FVLib code multi-processing capabilities are implemented based on the **shared-memory programming model** through the OpenMP application programming interface. It allows the development and deployment of portable and scalable intra-node parallel applications, but cannot take full advantage of modern HPC systems since inter-node communication, demanded to **simulate large-scale engineering applications** on meshes with several millions of cells, requires a **distributed-memory programming model**.

**_The first objective of the present advanced computing project proposal is to implement a distributed-memory parallel programming model in the FVLib code through the message-passing interface (MPI) paradigm_**. MPI has become a reliable and widely used standard for writing portable scalable large-scale parallel applications in modern HPC systems and is available in several open-source implementations (such as OpenMPI and MPICH). **_The second objective of the present advanced computing project proposal is to analyse a hybrid shared-memory/message-passing programming model_**, often discussed in the literature as a method for achieving better application performance on clusters of distributed-memory systems. Since the FVLib code already provides a shared-memory parallelisation, **combining OpenMP and MPI** (and therefore the shared-memory and message-passing models) shall be a straightforward step, although it requires careful analysis and optimisation.
