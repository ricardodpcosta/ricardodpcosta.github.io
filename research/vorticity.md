---
layout: page
title: Research
---

<p style="margin-bottom:1cm;"></p>

<div class="message">
  Short description on the major research topics of interest that I have investigated. Please refer to the <i>Curriculum Vitae</i> for a complete list.
</div>

---

### _Navier-Stokes equations in vorticity formulations_

<p style="margin-bottom:1cm;"></p>


The conventional mathematical models for simulating incompressible fluid flows are formulated using the Navier–Stokes equations in terms of velocity and pressure. In this setting, the **pressure–velocity coupling** is a central issue, and for decades numerous numerical strategies have been proposed to solve these equations efficiently and accurately. In 2D, an alternative consists in reformulating the Navier–Stokes equations in terms of two scalar variables—the **streamfunction and vorticity**—thereby reducing the number of unknowns from three (two velocity components and pressure) to two. A key advantage of this formulation is that it eliminates the need to compute pressure, thus avoiding the inherent difficulties of pressure–velocity coupling in the primitive variables approach. Moreover, the **continuity condition is automatically satisfied**, since the velocity components are derived directly from potential derivatives.

In the context of low-order accurate discretisations, the Navier–Stokes equations are conventionally solved using **segregated algorithms** such as SIMPLE or PISO. However, these approaches become computationally inefficient when applied with high-order discretisations. The common alternative is to solve the equations in a **coupled velocity–pressure system**, which is typically ill-conditioned, requires advanced preconditioners, and entails higher memory costs. By contrast, the streamfunction–vorticity formulation naturally leads to a system of partial differential equations that can be discretised and solved in a segregated manner even with high-order accurate methods. The main difficulty lies in the boundary conditions: while Dirichlet and Neumann conditions for the streamfunction follow directly from prescribed boundary velocities, no explicit condition exists for the vorticity. Furthermore, in **multiply connected domains**, compatibility conditions are required to ensure the streamfunction is well-defined on closed boundaries.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:60%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/streamfunction.png' | relative_url }}">
  </div>
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:60%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/vorticity.png' | relative_url }}">
  </div>
</div>
<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    Streamlines.
  </div>
  <div class="column" style="width:50%; text-align:center;">
    Vorticity contours.
  </div>
</div>

<p style="margin-bottom:1cm;"></p>

In \[[Costa et al., 2024](https://arxiv.org/abs/2506.05081)], we proposed a novel and efficient high-order accurate finite volume discretisation of the 2D incompressible Navier–Stokes equations in the streamfunction–vorticity formulation. Special attention is devoted to the derivation and numerical treatment of **appropriate boundary conditions** for both streamfunction and vorticity, including on **arbitrary curved boundaries**. To this end, the **ROD method** is employed, allowing curved boundaries to be represented with **linear piecewise elements**, while constrained polynomial reconstructions are used to rigorously enforce the prescribed boundary conditions, achieving up to **sixth-order convergence** on unstructured meshes.
