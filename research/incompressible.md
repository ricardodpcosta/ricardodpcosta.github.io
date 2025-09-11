---
layout: page
title: Research
---

### _Incompressible fluid flow problems_

<p style="margin-bottom:1cm;"></p>

The numerical solution of the **Navier–Stokes equations** is a cornerstone problem in computational fluid dynamics, enabling the simulation of countless engineering applications. In addition to the **momentum balance equation**, the system requires a **mass conservation equation** tailored to the flow regime. For incompressible flows, the **incompressibility constraint** (div–grad duality) enforces that the net mass rate of change vanishes within any control volume. Although conceptually straightforward, this constraint poses major challenges for the design of accurate, robust, and stable discretisations, particularly in the high-order context.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:60%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/pressure.png' | relative_url }}">
  </div>
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:60%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/streamlines.png' | relative_url }}">
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

<p style="margin-bottom:1cm;"></p>

Several stabilisation techniques have been developed in the context of first- and second-order methods, such as **staggered mesh** discretisations or the classical **Rhie–Chow interpolation** on collocated meshes for pressure–velocity coupling. These approaches, however, do not easily extend to high-order accuracy. In \[[Costa et al., 2017](https://doi.org/10.1007/s10915-016-0348-9); [Costa et al., 2017](https://doi.org/10.1016/j.jcp.2017.07.047)], we proposed a very high-order accurate finite volume method (FVM) based on specialised polynomial reconstructions built on a **staggered mesh** framework to consistently handle the **div–grad duality**. The resulting velocity–pressure coupled system is further accelerated by a novel **incomplete inverse preconditioning technique** based on the **Schur complement** for saddle-point matrices.

This work was later extended with the **ROD method** in \[[Costa et al., 2022](https://doi.org/10.1016/j.cma.2022.115064); [Costa et al., 2023](https://doi.org/10.1016/j.cma.2023.116274)] to address 2D and 3D incompressible flows on **arbitrary curved boundaries**, achieving up to **sixth-order convergence** on unstructured meshes with a piecewise linear boundary approximation.
