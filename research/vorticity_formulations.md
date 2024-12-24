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

The conventional mathematical models to simulate incompressible fluid flow problems are formulated based on the Navier-Stokes equations written in terms of pressure and velocity. In that regard, the **pressure-velocity coupling** is a fundamental issue and, for decades, researchers have developed uncountable numerical techniques and methods to efficiently and accurately solve these equations.

In two dimensions, a different approach consists in rewriting the Navier-Stokes equations in terms of two scalar quantities, the **streamfunction and vorticity**, reducing the number of variables from three (two velocity components and pressure) to two (streamfunction and vorticity). More interestingly, the streamfunction-vorticity formulation does not require pressure to be computed and, therefore, the inherent difficulties associated with the pressure-velocity coupling in the primitive variables formulation are avoided. Moreover, the **continuity condition is always satisfied** as velocity components are determined from the potential derivatives.

In the context of low-order accurate discretisation methods, the conventional practice is to solve the Navier-Stokes equations through **segregated algorithms**, such as SIMPLE and PISO. These approaches are, unfortunately, found to be computationally inefficient when high-order accurate discretisation methods are employed. Thus, the conventional practice is to solve the Navier-Stokes equations in a **coupled linear system of pressure and velocity**, which is typically ill-conditioned. This makes the solution procedure more difficult, even with the use of sophisticated preconditioners, besides the higher memory consumption. In contrast, another noteworthy aspect of the Navier-Stokes equations in streamfunction-vorticity variables is that the system of partial differential equations can be readily discretised independently and solved in a segregated algorithm, even when high-order accurate discretisation methods are employed.

Unfortunately, the system of partial differential equations comes with an unusual configuration since Dirichlet and Neumann boundary conditions are straightforwardly obtained for the streamfunction from the prescribed boundary velocity but none exists for the vorticity. Moreover, compatibility conditions are required in **multiply connected domains** such that the prescribed streamfunction value on closed boundaries is well-defined.

In [[Costa et al., 2024]()], a novel and efficient high-order accurate finite volume discretisation of the two-dimensional incompressible Navier-Stokes equations in the streamfunction-vorticity formulation is proposed. A careful discussion is devoted to **deriving appropriate boundary conditions** for the streamfunction and vorticity and their numerical treatment, including on **arbitrary curved boundaries**. For that, the **ROD method** is employed, allowing **arbitrary curved boundaries** to be approximated with **linear piecewise elements**, while polynomial reconstructions with specific linear constraints are computed to fulfil the prescribed boundary conditions.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:70%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/psi.png' | relative_url }}">
  </div>
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:70%; display:block; margin-left:auto; margin-right:auto;" src="{{ '/public/omega.png' | relative_url }}">
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

---
