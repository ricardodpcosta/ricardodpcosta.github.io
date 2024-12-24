---
layout: page
title: Research
---

<p style="margin-bottom:1cm;"></p>

<div class="message">
  Short description on the major research topics of interest that I have investigated. Please refer to the <i>Curriculum Vitae</i> for a complete list.
</div>

---

### _Incompressible fluid flow problems_

<p style="margin-bottom:1cm;"></p>

The numerical solution of the **Navier-Stokes equations** is a fundamental problem in computational fluid dynamics, enabling the numerical simulation of uncountable real engineering applications. Besides the **momentum balance equation**, the system requires a **mass conservation equation** specified depending on the flow dynamics. For incompressible flows, the **incompressibility constraint** (div-grad duality) specifies that the mass rate of change equals zero in any control volume. Although conceptually simple, the incompressibility constraint raises significant challenges for developing accurate, robust, and stable discretisations, particularly in the high-order accurate context.

Several stabilisation techniques were developed in the context of first- and second-orders accurate methods, such as discretisation on **staggered meshes** or the classical Rhie-Chow interpolation on **collocated meshes** for the pressure-velocity coupling. These techniques cannot, however, be easily extended for achieving high-order of convergence. In [[Costa et al., 2017](https://doi.org/10.1007/s10915-016-0348-9); [Costa et al., 2017](https://doi.org/10.1016/j.jcp.2017.07.047)], a very high-order accurate method is proposed in the FVM paradigm based on specific polynomial reconstructions computed on a **staggered mesh** construction to handle the **div-grad duality**. The solution of the resulting velocity-pressure coupled system is also accelerated with a novel **incomplete inverse preconditioning technique** based on the **Schur complement** for saddle-point matrices. The work is further improved and equipped with the **ROD method** in [[Costa et al., 2022](https://doi.org/10.1016/j.cma.2022.115064); [Costa et al., 2023](https://doi.org/10.1016/j.cma.2023.116274)] to solve 2D and 3D incompressible fluid flow problems in **arbitrary curved boundaries**, effectively achieving the sixth-order of convergence on unstructured meshes.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:70%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/pressure.png' | relative_url }}">
  </div>
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:70%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/streamlines.png' | relative_url }}">
  </div>
</div>
<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    Pressure distribution.
  </div>
  <div class="column" style="width:50%; text-align:center;">
    Velocity streamlines.
  </div>
</div>
