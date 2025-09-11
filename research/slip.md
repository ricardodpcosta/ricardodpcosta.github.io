---
layout: page
title: Research
---

### _General slip boundary conditions_

<p style="margin-bottom:1cm;"></p>

The conventional **no-slip boundary condition** fails to hold in many fluid flow problems and must be replaced with appropriate **slip boundary conditions** that account for wall and fluid properties. From inviscid to viscoelastic flows, the correct imposition of slip boundary conditions is essential in numerous engineering applications. These conditions remain a subject of debate among fluid dynamicists and pose significant numerical challenges, particularly when pursuing very **high-order accurate** methods.

The available literature on general slip boundary conditions is limited, and existing approaches typically achieve only first- or second-order convergence. The complexity increases substantially on **curved boundaries**, since the tangential component of the fluid traction vector depends on the boundary line curvature. In 3D, the challenge becomes even greater, as both principal surface curvatures must be considered.

<p style="margin-bottom:1cm;"></p>

<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:60%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/minimum_curvature.png' | relative_url }}">
  </div>
  <div class="column" style="width:50%; text-align:center;">
    <img style="width:60%; display:block; margin-left:auto; margin-right:auto;" src="{{ 'public/maximum_curvature.png' | relative_url }}">
  </div>
</div>
<div class="row">
  <div class="column" style="width:50%; text-align:center;">
    Boundary minimum curvature.
  </div>
  <div class="column" style="width:50%; text-align:center;">
    Boundary maximum curvature.
  </div>
</div>

<p style="margin-bottom:1cm;"></p>

In \[[Costa et al., 2023](https://doi.org/10.1016/j.cma.2023.116274)], we proposed a simple, efficient, and very high-order accurate method within the finite volume (FVM) framework to impose **general slip boundary conditions** on **arbitrary curved boundaries** for 3D fluid flow problems governed by the **incompressible Navier–Stokes equations**. Building on previous work, the pressure–velocity coupling is handled using a staggered mesh discretisation, ensuring stable and accurate treatment of the **div–grad duality**. On curved boundaries, the slip conditions are reformulated in a local reference system, enabling the direct application of the **ROD method**, which achieves up to **eighth-order convergence** on unstructured meshes with a piecewise linear boundary approximation.
